```csharp
// 获得选中的gameobject
Selection.gameObjects
Selection.activeGameObject
// 从Object获得prefab
PrefabUtility.GetCorrespondingObjectFromSource
// 从prefab获得根物体
PrefabUtility.FindPrefabRoot(prefab)
// 刷新Project视窗
UnityEditor.AssetDatabase.Refresh
// 替换文件或文件夹
UnityEditor.FileUtil.ReplaceFile
UnityEditor.FileUtil.ReplaceDirectory
// 使用实例创建prefab并连接
PrefabUtility.SaveAsPrefabAssetAndConnect
PrefabUtility.SaveAsPrefabAsset
// 选中
EditorGUIUtility.PingObject(obj);

// 预制体，且不在场景中 is a prefab in asset
var IsPartOfPrefabAsset = PrefabUtility.IsPartOfPrefabAsset(gameObject);
// 预制体，且在场景中   is a prefab in hierarchy(scene) as instance
var IsPartOfPrefabInstance = PrefabUtility.IsPartOfPrefabInstance(gameObject);
private void OnTransformChildrenChanged()
{
    Debug.Log("Children changed! note: child of children changed won't call this function");
}
// 请求刷新布局
LayoutRebuilder.MarkLayoutForRebuild(GetComponent<RectTransform>());
// 强制刷新布局
LayoutRebuilder.ForceRebuildLayoutImmediate(GetComponent<RectTransform>());
// 通过InstanceID获得Object，主要用于序列化
EditorUtility.InstanceIDToObject
```