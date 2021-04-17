---
description: La interfaz ITAudioDeviceControl expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interfaz ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680940"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="f84f8-103">Interfaz ITAudioDeviceControl</span><span class="sxs-lookup"><span data-stu-id="f84f8-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="f84f8-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f84f8-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f84f8-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f84f8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f84f8-106">La interfaz **ITAudioDeviceControl** expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f84f8-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="f84f8-107">Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="f84f8-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="f84f8-108">Se expone cuando una llamada utiliza estos proveedores de servicios o un proveedor de servicios de terceros que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="f84f8-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="f84f8-109">Para obtener un puntero a la interfaz **ITAudioDeviceControl** , llame a **QueryInterface** en la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) que controla el dispositivo de audio correspondiente a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f84f8-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="f84f8-110">El tipo de medio de la interfaz **ITStream** debe ser audio para que se exponga la interfaz **ITAudioDeviceControl** .</span><span class="sxs-lookup"><span data-stu-id="f84f8-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="f84f8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f84f8-111">Members</span></span>

<span data-ttu-id="f84f8-112">La interfaz **ITAudioDeviceControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f84f8-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f84f8-113">**ITAudioDeviceControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f84f8-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="f84f8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f84f8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f84f8-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f84f8-115">Methods</span></span>

<span data-ttu-id="f84f8-116">La interfaz **ITAudioDeviceControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f84f8-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="f84f8-117">Método</span><span class="sxs-lookup"><span data-stu-id="f84f8-117">Method</span></span>                                              | <span data-ttu-id="f84f8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f84f8-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f84f8-119">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="f84f8-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="f84f8-120">Obtiene el valor de una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="f84f8-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="f84f8-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="f84f8-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="f84f8-122">Obtiene el intervalo de valores válidos para una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="f84f8-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="f84f8-123">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="f84f8-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="f84f8-124">Establece el valor de una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="f84f8-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f84f8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f84f8-125">Requirements</span></span>



| <span data-ttu-id="f84f8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f84f8-126">Requirement</span></span> | <span data-ttu-id="f84f8-127">Value</span><span class="sxs-lookup"><span data-stu-id="f84f8-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f84f8-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f84f8-128">TAPI version</span></span><br/> | <span data-ttu-id="f84f8-129">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f84f8-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f84f8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f84f8-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f84f8-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f84f8-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f84f8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f84f8-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f84f8-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f84f8-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f84f8-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f84f8-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f84f8-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f84f8-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f84f8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f84f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84f8-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="f84f8-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

