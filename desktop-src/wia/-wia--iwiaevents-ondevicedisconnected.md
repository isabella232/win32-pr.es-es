---
description: Evento que tiene lugar cuando se desconecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276866"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="c3ee1-103">Evento WIA. OnDeviceDisconnected</span><span class="sxs-lookup"><span data-stu-id="c3ee1-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="c3ee1-104">Evento que tiene lugar cuando se desconecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="c3ee1-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ee1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3ee1-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="c3ee1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ee1-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="c3ee1-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="c3ee1-108">Cadena que contiene el identificador del dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="c3ee1-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ee1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3ee1-109">Return value</span></span>

<span data-ttu-id="c3ee1-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c3ee1-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ee1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3ee1-111">Remarks</span></span>

<span data-ttu-id="c3ee1-112">WIA notifica al script o a la aplicación cada vez que un dispositivo de hardware se desconecta del equipo.</span><span class="sxs-lookup"><span data-stu-id="c3ee1-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="c3ee1-113">Implemente la subrutina **objWia** \_ **OnDeviceDisconnected ()** para permitir que el script o la aplicación respondan a la desconexión del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3ee1-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="c3ee1-114">Por ejemplo, puede que desee un script para actualizar la recopilación de [**dispositivos**](-wia-iwia-devices.md) cuando se quita un dispositivo del equipo.</span><span class="sxs-lookup"><span data-stu-id="c3ee1-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ee1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ee1-115">Requirements</span></span>



| <span data-ttu-id="c3ee1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ee1-116">Requirement</span></span> | <span data-ttu-id="c3ee1-117">Value</span><span class="sxs-lookup"><span data-stu-id="c3ee1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ee1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3ee1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ee1-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c3ee1-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3ee1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3ee1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ee1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3ee1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c3ee1-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3ee1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3ee1-123"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c3ee1-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




