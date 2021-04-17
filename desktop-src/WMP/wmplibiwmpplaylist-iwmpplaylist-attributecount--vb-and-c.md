---
title: Propiedad attributeCount de IWMPPlaylist
description: La propiedad attributeCount obtiene el número de atributos asociados a una lista de reproducción.
ms.assetid: 0713ec4e-7e06-4ad2-8f7c-17ed5a92d5ee
keywords:
- propiedades de attributeCount Media Player de Windows
- propiedad attributeCount de Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, propiedad attributeCount
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4107eb1ad302415715b573b55d2dee1d7155128d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700000"
---
# <a name="iwmpplaylistattributecount-property"></a><span data-ttu-id="c3f31-106">IWMPPlaylist:: attributeCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c3f31-106">IWMPPlaylist::attributeCount property</span></span>

<span data-ttu-id="c3f31-107">La propiedad **attributeCount** obtiene el número de atributos asociados a una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c3f31-107">The **attributeCount** property gets the number of attributes associated with a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f31-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3f31-108">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get; set;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c3f31-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c3f31-109">Property value</span></span>

<span data-ttu-id="c3f31-110">**System. Int32** que es el número de atributos asociados a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c3f31-110">A **System.Int32** that is the number of attributes associated with the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f31-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3f31-111">Remarks</span></span>

<span data-ttu-id="c3f31-112">Dado que las listas de reproducción pueden provienen de muchos orígenes diferentes, pueden tener varios conjuntos de atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c3f31-112">Because playlists can come from many different sources, they can have several different sets of attributes.</span></span> <span data-ttu-id="c3f31-113">Esta propiedad obtiene el número total de atributos asociados a una lista de reproducción determinada para que otros miembros de la interfaz **IWMPPlaylist** puedan tener acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="c3f31-113">This property gets the total number of attributes associated with a particular playlist so that other members of the **IWMPPlaylist** interface can access them.</span></span>

<span data-ttu-id="c3f31-114">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c3f31-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="c3f31-115">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c3f31-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c3f31-116">Para obtener más información sobre los atributos compatibles con Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c3f31-116">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c3f31-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c3f31-117">Examples</span></span>

<span data-ttu-id="c3f31-118">En el ejemplo siguiente se muestra cómo se usan varias propiedades y métodos de las interfaces **IWMPPlaylist** y **IWMPMedia** rellenando un control TreeView con nodos para la lista de reproducción actual, atributos de la lista de reproducción, elementos multimedia de la lista de reproducción y atributos de elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="c3f31-118">The following example illustrates how various properties and methods of the **IWMPPlaylist** and **IWMPMedia** interfaces are used by filling a treeview control with nodes for the current playlist, playlist attributes, media items in the playlist, and media item attributes.</span></span> <span data-ttu-id="c3f31-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="c3f31-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
WMPLib.IWMPPlaylist playlist = player.currentPlaylist;
WMPLib.IWMPMedia media;
string name;

// Demonstrates setItemInfo()
playlist.setItemInfo("custom playlist attribute", "changed");
playlist.get_Item(0).setItemInfo("new custom attribute", "5");

// Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
System.Windows.Forms.TreeNode playlistRootNode = new System.Windows.Forms.TreeNode("Playlist Attributes");

for (int i = 0; i < playlist.attributeCount; ++i)
{
    // Add a tree node for each playlist attribute.
    string attribute = playlist.get_attributeName(i);
    playlistRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(attribute));

    // Add a subnode for the item info for that attribute.
    string info = playlist.getItemInfo(attribute);
    playlistRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(info));
}

// Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode);

// Add nodes for each media item and subnodes for each attribute of that item.
System.Windows.Forms.TreeNode mediaRootNode = new System.Windows.Forms.TreeNode("Media Items in the Playlist");
for(int i = 0; i < playlist.count; i++)
{
    // Get the media item
    media = playlist.get_Item(i);

    // Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(media.name));

    // Add a child node for each attribute of the media item
    for(int j = 0; j < media.attributeCount; j++)
    {
        name = media.getAttributeName(j);
        mediaRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(name + ": " + media.getItemInfo(name)));
    }
}

// Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode);
```


```VB

Dim playlist As WMPLib.IWMPPlaylist = player.currentPlaylist
Dim Media As WMPLib.IWMPMedia
Dim name As String

&#39; Demonstrates setItemInfo()
playlist.setItemInfo(&quot;custom playlist attribute&quot;, &quot;changed&quot;)
playlist.Item(0).setItemInfo(&quot;new custom attribute&quot;, &quot;5&quot;)

&#39; Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
Dim playlistRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Playlist Attributes&quot;)

For i As Integer = 0 To (playlist.attributeCount - 1) Step 1

    &#39; Add a tree node for each playlist attribute.
    Dim attribute As String = playlist.attributeName(i)
    playlistRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(attribute))

    &#39; Add a subnode for the item info for that attribute.
    Dim info As String = playlist.getItemInfo(attribute)
    playlistRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(info))

Next i

&#39; Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode)

&#39; Add nodes for each media item and subnodes for each attribute of that item.
Dim mediaRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Media Items in the Playlist&quot;)

For i As Integer = 0 To (playlist.count - 1) Step 1

    &#39; Get the media item
    Media = playlist.Item(i)

    &#39; Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(Media.name))

    &#39; Add a child node for each attribute of the media item
    For j As Integer = 0 To (Media.attributeCount - 1) Step 1

        name = Media.getAttributeName(j)
        mediaRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(name + &quot;: &quot; + Media.getItemInfo(name)))

    Next j

Next i

&#39; Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode)
```





## <a name="requirements"></a><span data-ttu-id="c3f31-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3f31-120">Requirements</span></span>



| <span data-ttu-id="c3f31-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f31-121">Requirement</span></span> | <span data-ttu-id="c3f31-122">Value</span><span class="sxs-lookup"><span data-stu-id="c3f31-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f31-123">Versión</span><span class="sxs-lookup"><span data-stu-id="c3f31-123">Version</span></span><br/>   | <span data-ttu-id="c3f31-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c3f31-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c3f31-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3f31-125">Namespace</span></span><br/> | <span data-ttu-id="c3f31-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3f31-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c3f31-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c3f31-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3f31-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f31-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f31-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3f31-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f31-130">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f31-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





