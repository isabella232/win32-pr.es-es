---
description: La interfaz ITAudioSettings expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaz ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690784"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="2d07e-103">Interfaz ITAudioSettings</span><span class="sxs-lookup"><span data-stu-id="2d07e-103">ITAudioSettings interface</span></span>

<span data-ttu-id="2d07e-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2d07e-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d07e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2d07e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2d07e-106">La interfaz **ITAudioSettings** expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2d07e-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="2d07e-107">Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="2d07e-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="2d07e-108">Solo se expone cuando una llamada utiliza estos proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="2d07e-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="2d07e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d07e-109">Members</span></span>

<span data-ttu-id="2d07e-110">La interfaz **ITAudioSettings** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d07e-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d07e-111">**ITAudioSettings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d07e-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="2d07e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d07e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d07e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d07e-113">Methods</span></span>

<span data-ttu-id="2d07e-114">La interfaz **ITAudioSettings** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2d07e-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="2d07e-115">Método</span><span class="sxs-lookup"><span data-stu-id="2d07e-115">Method</span></span>                                              | <span data-ttu-id="2d07e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d07e-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d07e-117">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="2d07e-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="2d07e-118">Obtiene el valor de una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="2d07e-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="2d07e-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="2d07e-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="2d07e-120">Obtiene el intervalo de valores válidos para una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="2d07e-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="2d07e-121">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="2d07e-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="2d07e-122">Establece el valor de una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="2d07e-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2d07e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d07e-123">Requirements</span></span>



| <span data-ttu-id="2d07e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d07e-124">Requirement</span></span> | <span data-ttu-id="2d07e-125">Value</span><span class="sxs-lookup"><span data-stu-id="2d07e-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d07e-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2d07e-126">TAPI version</span></span><br/> | <span data-ttu-id="2d07e-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2d07e-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2d07e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d07e-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2d07e-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d07e-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d07e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d07e-130">Library</span></span><br/>      | <dl> <span data-ttu-id="2d07e-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d07e-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2d07e-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d07e-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="2d07e-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d07e-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

