---
description: Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276867"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="d6646-103">Evento WIA. OnDeviceConnected</span><span class="sxs-lookup"><span data-stu-id="d6646-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="d6646-104">Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="d6646-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6646-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6646-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="d6646-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6646-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6646-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="d6646-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d6646-108">Cadena que contiene el identificador del dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="d6646-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6646-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6646-109">Return value</span></span>

<span data-ttu-id="d6646-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d6646-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6646-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6646-111">Remarks</span></span>

<span data-ttu-id="d6646-112">WIA notifica al script o a la aplicación cada vez que se conecta un nuevo dispositivo de hardware al equipo.</span><span class="sxs-lookup"><span data-stu-id="d6646-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="d6646-113">Implemente la \_ subrutina objWia **OnDeviceConnected ()** para permitir que el script o la aplicación respondan a la conexión del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6646-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="d6646-114">Por ejemplo, puede que desee un script para actualizar la recopilación de [**dispositivos**](-wia-iwia-devices.md) cuando se instala un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6646-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6646-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6646-115">Requirements</span></span>



| <span data-ttu-id="d6646-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6646-116">Requirement</span></span> | <span data-ttu-id="d6646-117">Value</span><span class="sxs-lookup"><span data-stu-id="d6646-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6646-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6646-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6646-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d6646-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6646-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6646-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6646-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6646-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d6646-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6646-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6646-123"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d6646-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




