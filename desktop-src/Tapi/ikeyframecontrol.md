---
description: La interfaz IKeyFrameControl se implementa mediante H. 323 MSP y solo está disponible en objetos de secuencia H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interfaz IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690527"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="4d843-103">Interfaz IKeyFrameControl</span><span class="sxs-lookup"><span data-stu-id="4d843-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="4d843-104">\[**IKeyFrameControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d843-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d843-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4d843-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4d843-106">La interfaz **IKeyFrameControl** se implementa mediante [h. 323 MSP](h323-msp.md) y solo está disponible en objetos de secuencia h. 323.</span><span class="sxs-lookup"><span data-stu-id="4d843-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="4d843-107">Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.</span><span class="sxs-lookup"><span data-stu-id="4d843-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="4d843-108">Tiene dos métodos que permiten que la aplicación solicite al punto de conexión remoto que actualice la imagen de vídeo con un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="4d843-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="4d843-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d843-109">Members</span></span>

<span data-ttu-id="4d843-110">La interfaz **IKeyFrameControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4d843-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4d843-111">**IKeyFrameControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d843-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="4d843-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d843-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4d843-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d843-113">Methods</span></span>

<span data-ttu-id="4d843-114">La interfaz **IKeyFrameControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4d843-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="4d843-115">Método</span><span class="sxs-lookup"><span data-stu-id="4d843-115">Method</span></span>                                                                  | <span data-ttu-id="4d843-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d843-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d843-117">**PeriodicUpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="4d843-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="4d843-118">Configura un temporizador en la secuencia que pedirá actualizaciones de imágenes periódicamente.</span><span class="sxs-lookup"><span data-stu-id="4d843-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="4d843-119">**UpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="4d843-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="4d843-120">Pide al remitente del vídeo que actualice la imagen.</span><span class="sxs-lookup"><span data-stu-id="4d843-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="4d843-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d843-121">Requirements</span></span>



| <span data-ttu-id="4d843-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d843-122">Requirement</span></span> | <span data-ttu-id="4d843-123">Value</span><span class="sxs-lookup"><span data-stu-id="4d843-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d843-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4d843-124">TAPI version</span></span><br/> | <span data-ttu-id="4d843-125">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4d843-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4d843-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d843-126">Header</span></span><br/>       | <dl> <span data-ttu-id="4d843-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d843-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="4d843-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d843-128">Library</span></span><br/>      | <dl> <span data-ttu-id="4d843-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d843-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4d843-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d843-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="4d843-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d843-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4d843-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d843-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d843-133">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="4d843-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

