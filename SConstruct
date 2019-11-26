import excons
import excons.tools.maya as maya

maya.SetupMscver()

env = excons.MakeBaseEnv()

projs = [
   {"name": "grim_IK",
    "prefix": "maya/plug-ins/%s" % maya.Version(nice=True),
    "bldprefix": maya.Version(),
    "type": "dynamicmodule",
    "ext": maya.PluginExt(),
    "srcs": ["grim_vik.cpp", "plugin_main.cpp"],
    "install": {"maya/scripts": ["AEgrim_vikTemplate.mel"]},
    "custom": [maya.Require]}
]


excons.DeclareTargets(env, projs)