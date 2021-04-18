---
description: La propiedad Children del objeto Item recupera una colección de objetos Item. Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico. Solo lectura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720389"
---
# <a name="itemchildren-property"></a><span data-ttu-id="d306d-105">Item. Children (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d306d-105">Item.Children property</span></span>

<span data-ttu-id="d306d-106">La propiedad **Children** del objeto [**Item**](-wia-item.md) recupera una colección de objetos **Item** .</span><span class="sxs-lookup"><span data-stu-id="d306d-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="d306d-107">Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico.</span><span class="sxs-lookup"><span data-stu-id="d306d-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="d306d-108">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d306d-108">Read-only.</span></span>

<span data-ttu-id="d306d-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d306d-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d306d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d306d-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="d306d-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d306d-111">Property value</span></span>

<span data-ttu-id="d306d-112">Variable que recibe los objetos.</span><span class="sxs-lookup"><span data-stu-id="d306d-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="d306d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d306d-113">Remarks</span></span>

<span data-ttu-id="d306d-114">Use esta propiedad para navegar por el árbol jerárquico de objetos de [**elemento**](-wia-item.md) que representan un dispositivo, las carpetas y los archivos que residen en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d306d-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="d306d-115">La propiedad **Children** es una colección de objetos de [**elemento**](-wia-item.md) solo del nivel que se encuentra directamente debajo de este objeto de **elemento** en el árbol.</span><span class="sxs-lookup"><span data-stu-id="d306d-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="d306d-116">Para navegar más abajo por el árbol, use esta propiedad de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="d306d-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="d306d-117">Si el elemento no puede o no tiene ningún elemento secundario, esta propiedad devuelve una colección vacía.</span><span class="sxs-lookup"><span data-stu-id="d306d-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="d306d-118">Esta colección está basada en 0.</span><span class="sxs-lookup"><span data-stu-id="d306d-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d306d-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d306d-119">Examples</span></span>

<span data-ttu-id="d306d-120">En el ejemplo siguiente se muestra el uso de la propiedad **Children** para recuperar y enumerar una colección de los elementos secundarios de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d306d-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="d306d-121">Si el dispositivo es una cámara digital, la colección normalmente contiene elementos de carpeta e imagen.</span><span class="sxs-lookup"><span data-stu-id="d306d-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="d306d-122">Si el dispositivo es un escáner, la colección normalmente contiene elementos que representan las camas de digitalización.</span><span class="sxs-lookup"><span data-stu-id="d306d-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="d306d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d306d-123">Requirements</span></span>



| <span data-ttu-id="d306d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d306d-124">Requirement</span></span> | <span data-ttu-id="d306d-125">Value</span><span class="sxs-lookup"><span data-stu-id="d306d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d306d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d306d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d306d-127">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d306d-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d306d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d306d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d306d-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d306d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d306d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d306d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d306d-131"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d306d-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




