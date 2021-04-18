---
title: IWMPCdromCollection (método del elemento)
description: El método Item devuelve una interfaz IWMPCdrom en el índice especificado.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Método de elemento Media Player de Windows
- Método de elemento Windows Media Player, interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718806"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="cf5d8-106">IWMPCdromCollection:: Item (método)</span><span class="sxs-lookup"><span data-stu-id="cf5d8-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="cf5d8-107">El método **Item** devuelve una interfaz **IWMPCdrom** en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5d8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf5d8-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="cf5d8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf5d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf5d8-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf5d8-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5d8-111">**System. Int32** que es el índice.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf5d8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf5d8-112">Return value</span></span>

<span data-ttu-id="cf5d8-113">Una interfaz **WMPLib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="cf5d8-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf5d8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf5d8-114">Remarks</span></span>

<span data-ttu-id="cf5d8-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="cf5d8-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cf5d8-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cf5d8-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cf5d8-117">Examples</span></span>

<span data-ttu-id="cf5d8-118">En el ejemplo siguiente se usa el **elemento** para mostrar el especificador de unidad y el nombre de lista de reproducción de cada CD disponible en el equipo en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="cf5d8-119">Si la unidad contiene realmente contenido de DVD, se requiere Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="cf5d8-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="cf5d8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf5d8-121">Requirements</span></span>



| <span data-ttu-id="cf5d8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf5d8-122">Requirement</span></span> | <span data-ttu-id="cf5d8-123">Value</span><span class="sxs-lookup"><span data-stu-id="cf5d8-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5d8-124">Versión</span><span class="sxs-lookup"><span data-stu-id="cf5d8-124">Version</span></span><br/>   | <span data-ttu-id="cf5d8-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="cf5d8-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cf5d8-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf5d8-126">Namespace</span></span><br/> | <span data-ttu-id="cf5d8-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cf5d8-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="cf5d8-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf5d8-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf5d8-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf5d8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf5d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf5d8-131">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-132">**Interfaz IWMPCdromCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-133">**IWMPCdromCollection. Count (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-134">**IWMPCdromCollection. getByDriveSpecifier (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-135">**IWMPPlaylist.name (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-136">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf5d8-137">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cf5d8-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





