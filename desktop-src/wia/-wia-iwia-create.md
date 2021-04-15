---
description: El método Create del objeto WIA establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado y devuelve un objeto de elemento que representa el dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545558"
---
# <a name="wiacreate-method"></a><span data-ttu-id="166ee-103">WIA. Create (método)</span><span class="sxs-lookup"><span data-stu-id="166ee-103">Wia.Create method</span></span>

<span data-ttu-id="166ee-104">El método **Create** del objeto [**WIA**](-wia-wia.md) establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="166ee-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="166ee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="166ee-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="166ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="166ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166ee-107">*Dispositivo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="166ee-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166ee-108">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="166ee-108">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="166ee-109">Especifica el dispositivo WIA al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="166ee-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="166ee-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="166ee-110">Return value</span></span>

<span data-ttu-id="166ee-111">Tipo: _ *IWiaDispatchItem*\*</span><span class="sxs-lookup"><span data-stu-id="166ee-111">Type: _ *IWiaDispatchItem*\*</span></span>

<span data-ttu-id="166ee-112">Si es correcto, este método devuelve un objeto de [**elemento**](-wia-item.md) que representa un dispositivo de hardware WIA (un elemento raíz).</span><span class="sxs-lookup"><span data-stu-id="166ee-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="166ee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="166ee-113">Remarks</span></span>

<span data-ttu-id="166ee-114">El parámetro *Device* especifica un objeto [**DeviceInfo**](-wia-deviceinfo.md) pasando el propio objeto, su índice de un objeto de colección o el valor de su propiedad [**ID**](-wia-iwiadeviceinfo-id.md) .</span><span class="sxs-lookup"><span data-stu-id="166ee-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="166ee-115">No pasar **nada** para mostrar un cuadro de diálogo que permita al usuario seleccionar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="166ee-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="166ee-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="166ee-116">Examples</span></span>

<span data-ttu-id="166ee-117">Los siguientes ejemplos de VBScript muestran el uso del método **Create** .</span><span class="sxs-lookup"><span data-stu-id="166ee-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="166ee-118">En el primer ejemplo se pasa un objeto [**DeviceInfo**](-wia-deviceinfo.md) al método **Create** .</span><span class="sxs-lookup"><span data-stu-id="166ee-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="166ee-119">Tenga en cuenta que al pasar la propiedad [**ID**](-wia-iwiadeviceinfo-id.md) del objeto se produce exactamente el mismo comportamiento.</span><span class="sxs-lookup"><span data-stu-id="166ee-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="166ee-120">En el ejemplo siguiente, la aplicación que realiza la llamada pasa el índice del objeto [**DeviceInfo**](-wia-deviceinfo.md) de la colección al método **Create** .</span><span class="sxs-lookup"><span data-stu-id="166ee-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="166ee-121">En el ejemplo siguiente se pasa **Nothing** al método **Create** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="166ee-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="166ee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="166ee-122">Requirements</span></span>



| <span data-ttu-id="166ee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="166ee-123">Requirement</span></span> | <span data-ttu-id="166ee-124">Value</span><span class="sxs-lookup"><span data-stu-id="166ee-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="166ee-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="166ee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="166ee-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="166ee-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="166ee-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="166ee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="166ee-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="166ee-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="166ee-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="166ee-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="166ee-130"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="166ee-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




