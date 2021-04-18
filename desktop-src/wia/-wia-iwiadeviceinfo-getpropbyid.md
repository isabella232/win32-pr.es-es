---
description: El método GetPropById del objeto DeviceInfo usa el identificador de una propiedad de dispositivo para devolver su valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. GetPropById, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720539"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="e4261-103">DeviceInfo. GetPropById, método</span><span class="sxs-lookup"><span data-stu-id="e4261-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="e4261-104">El método **GetPropById** del objeto [**DEVICEINFO**](-wia-deviceinfo.md) usa el identificador de una propiedad de dispositivo para devolver su valor.</span><span class="sxs-lookup"><span data-stu-id="e4261-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4261-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4261-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="e4261-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4261-107">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e4261-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4261-108">Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="e4261-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="e4261-109">Especifica el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e4261-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4261-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4261-110">Return value</span></span>

<span data-ttu-id="e4261-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="e4261-111">Type: **VARIANT**</span></span>

<span data-ttu-id="e4261-112">Este método devuelve el valor de la propiedad especificada por *ID*.</span><span class="sxs-lookup"><span data-stu-id="e4261-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4261-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4261-113">Remarks</span></span>

<span data-ttu-id="e4261-114">Use este método para buscar el valor de una propiedad de dispositivo de su identificador.</span><span class="sxs-lookup"><span data-stu-id="e4261-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="e4261-115">Para obtener una lista de identificadores de propiedad, vea [definiciones de constantes de propiedad de WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e4261-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="e4261-116">Para obtener información sobre las propiedades de adquisición de imágenes de Windows (WIA), consulte [constantes de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e4261-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="e4261-117">En el caso de las aplicaciones de Microsoft Visual Basic, agregue una referencia a "biblioteca de tipos 1,01 de adquisición de imágenes de Windows".</span><span class="sxs-lookup"><span data-stu-id="e4261-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="e4261-118">Las siguientes constantes definidas en ese archivo son válidas para este método:</span><span class="sxs-lookup"><span data-stu-id="e4261-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="e4261-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e4261-119">Examples</span></span>

<span data-ttu-id="e4261-120">En el ejemplo siguiente se muestra el uso del método **GetPropById** para recuperar un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e4261-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="e4261-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4261-121">Requirements</span></span>



| <span data-ttu-id="e4261-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4261-122">Requirement</span></span> | <span data-ttu-id="e4261-123">Value</span><span class="sxs-lookup"><span data-stu-id="e4261-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4261-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4261-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4261-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e4261-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4261-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4261-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4261-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4261-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e4261-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4261-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4261-129"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e4261-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




