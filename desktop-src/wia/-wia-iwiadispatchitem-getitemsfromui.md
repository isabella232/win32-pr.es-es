---
description: El método GetItemsFromUI del objeto Item muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154865"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="c7efe-103">Item. GetItemsFromUI (método)</span><span class="sxs-lookup"><span data-stu-id="c7efe-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="c7efe-104">El método **GetItemsFromUI** del objeto [**Item**](-wia-item.md) muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7efe-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7efe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7efe-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="c7efe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7efe-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c7efe-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7efe-108">Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="c7efe-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="c7efe-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="c7efe-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c7efe-110">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c7efe-110">Default.</span></span> <span data-ttu-id="c7efe-111">\[en \] especifica el comportamiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7efe-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="c7efe-112">Los valores válidos para este parámetro son los mismos que para el parámetro *lFlags* del método [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .</span><span class="sxs-lookup"><span data-stu-id="c7efe-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c7efe-113">*Intención* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7efe-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7efe-114">Tipo: **WiaIntent**</span><span class="sxs-lookup"><span data-stu-id="c7efe-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="c7efe-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="c7efe-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c7efe-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c7efe-116">Default.</span></span> <span data-ttu-id="c7efe-117">\[en \] especifica qué tipo de datos pretende representar la imagen.</span><span class="sxs-lookup"><span data-stu-id="c7efe-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="c7efe-118">Para obtener una lista de valores de intención de imagen, vea [**constantes de intención de imagen**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="c7efe-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7efe-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7efe-119">Return value</span></span>

<span data-ttu-id="c7efe-120">Tipo: **ICollection**</span><span class="sxs-lookup"><span data-stu-id="c7efe-120">Type: **ICollection**</span></span>

<span data-ttu-id="c7efe-121">Este método devuelve una colección de objetos de [**elemento**](-wia-item.md) que representan los elementos seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c7efe-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="c7efe-122">Si no se selecciona ningún elemento, la colección está vacía.</span><span class="sxs-lookup"><span data-stu-id="c7efe-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7efe-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7efe-123">Remarks</span></span>

<span data-ttu-id="c7efe-124">En el caso de las aplicaciones de Microsoft Visual Basic, agregue una referencia a "biblioteca de tipos 1,01 de adquisición de imágenes de Windows".</span><span class="sxs-lookup"><span data-stu-id="c7efe-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="c7efe-125">Este método solo se aplica a los dispositivos (elementos raíz).</span><span class="sxs-lookup"><span data-stu-id="c7efe-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="c7efe-126">El método devuelve una colección de objetos de [**elemento**](-wia-item.md) que representan las imágenes o los clips de audio seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c7efe-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="c7efe-127">Si el usuario no selecciona ningún elemento, el método devuelve una colección vacía.</span><span class="sxs-lookup"><span data-stu-id="c7efe-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="c7efe-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7efe-128">Examples</span></span>

<span data-ttu-id="c7efe-129">En el ejemplo siguiente se muestra el uso del método **GetItemsFromUI** para permitir que un usuario seleccione imágenes en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7efe-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="c7efe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7efe-130">Requirements</span></span>



| <span data-ttu-id="c7efe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7efe-131">Requirement</span></span> | <span data-ttu-id="c7efe-132">Value</span><span class="sxs-lookup"><span data-stu-id="c7efe-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7efe-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7efe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c7efe-134">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c7efe-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7efe-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7efe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c7efe-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7efe-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c7efe-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7efe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7efe-138"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c7efe-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




