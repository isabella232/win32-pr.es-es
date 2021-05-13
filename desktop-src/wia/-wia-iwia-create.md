---
description: El método Create del objeto Wia establece una conexión con el dispositivo Windows Image Acquisition (WIA) especificado y devuelve un objeto Item que representa el dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Método Wia.Create
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
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841336"
---
# <a name="wiacreate-method"></a><span data-ttu-id="77365-103">Método Wia.Create</span><span class="sxs-lookup"><span data-stu-id="77365-103">Wia.Create method</span></span>

<span data-ttu-id="77365-104">El **método Create** del objeto [**Wia**](-wia-wia.md) establece una conexión con el dispositivo Windows Image Acquisition (WIA) especificado y devuelve un objeto [**Item**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77365-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="77365-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77365-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="77365-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77365-107">*Dispositivo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="77365-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77365-108">Tipo: **\* VARIANT**</span><span class="sxs-lookup"><span data-stu-id="77365-108">Type: **VARIANT\***</span></span>

<span data-ttu-id="77365-109">Especifica el dispositivo WIA al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="77365-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77365-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77365-110">Return value</span></span>

<span data-ttu-id="77365-111">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="77365-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="77365-112">Si se realiza correctamente, este método devuelve un [**objeto Item**](-wia-item.md) que representa un dispositivo de hardware WIA (un elemento raíz).</span><span class="sxs-lookup"><span data-stu-id="77365-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="77365-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77365-113">Remarks</span></span>

<span data-ttu-id="77365-114">El *parámetro Device* especifica un objeto [**DeviceInfo**](-wia-deviceinfo.md) pasando el propio objeto, su índice de un objeto de colección o el valor de su [**propiedad Id.**](-wia-iwiadeviceinfo-id.md)</span><span class="sxs-lookup"><span data-stu-id="77365-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="77365-115">Pasar **nada** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77365-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="77365-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="77365-116">Examples</span></span>

<span data-ttu-id="77365-117">En los siguientes ejemplos de VBScript se muestra el uso del **método Create.**</span><span class="sxs-lookup"><span data-stu-id="77365-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="77365-118">En el primer ejemplo se pasa [**un objeto DeviceInfo**](-wia-deviceinfo.md) al **método Create.**</span><span class="sxs-lookup"><span data-stu-id="77365-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="77365-119">Tenga en cuenta que pasar la propiedad [**Id**](-wia-iwiadeviceinfo-id.md) del objeto produce exactamente el mismo comportamiento.</span><span class="sxs-lookup"><span data-stu-id="77365-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


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



<span data-ttu-id="77365-120">En el ejemplo siguiente, la aplicación que realiza la llamada pasa el índice del [**objeto DeviceInfo**](-wia-deviceinfo.md) de la colección al **método Create.**</span><span class="sxs-lookup"><span data-stu-id="77365-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


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



<span data-ttu-id="77365-121">En el ejemplo siguiente se **pasa Nothing** al **método Create** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77365-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="77365-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77365-122">Requirements</span></span>



| <span data-ttu-id="77365-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="77365-123">Requirement</span></span> | <span data-ttu-id="77365-124">Value</span><span class="sxs-lookup"><span data-stu-id="77365-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77365-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77365-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77365-126">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="77365-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77365-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77365-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77365-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="77365-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="77365-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77365-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77365-130"><dt>Wiascr.dll (versión 4.90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="77365-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




