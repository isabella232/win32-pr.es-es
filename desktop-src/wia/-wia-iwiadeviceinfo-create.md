---
description: El método Create del objeto DeviceInfo establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado por el objeto DeviceInfo y devuelve un objeto de elemento que representa el dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720398"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="58e7d-103">DeviceInfo. Create (método)</span><span class="sxs-lookup"><span data-stu-id="58e7d-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="58e7d-104">El método **Create** del objeto [**DeviceInfo**](-wia-deviceinfo.md) establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado por el objeto **DeviceInfo** y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58e7d-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58e7d-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="58e7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58e7d-106">Parameters</span></span>

<span data-ttu-id="58e7d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="58e7d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58e7d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58e7d-108">Return value</span></span>

<span data-ttu-id="58e7d-109">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="58e7d-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="58e7d-110">Este método devuelve el objeto de [**elemento**](-wia-item.md) que representa el dispositivo que se crea.</span><span class="sxs-lookup"><span data-stu-id="58e7d-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e7d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58e7d-111">Remarks</span></span>

<span data-ttu-id="58e7d-112">Use el método **Create** para crear una conexión a un dispositivo de hardware WIA después de enumerar la recopilación de [**dispositivos**](-wia-iwia-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="58e7d-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="58e7d-113">El método devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo (un elemento raíz).</span><span class="sxs-lookup"><span data-stu-id="58e7d-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="58e7d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="58e7d-114">Examples</span></span>

<span data-ttu-id="58e7d-115">En el siguiente ejemplo se muestra el uso del método **Create** .</span><span class="sxs-lookup"><span data-stu-id="58e7d-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="58e7d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58e7d-116">Requirements</span></span>



| <span data-ttu-id="58e7d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e7d-117">Requirement</span></span> | <span data-ttu-id="58e7d-118">Value</span><span class="sxs-lookup"><span data-stu-id="58e7d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e7d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58e7d-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="58e7d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58e7d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58e7d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="58e7d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="58e7d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58e7d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e7d-124"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="58e7d-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




