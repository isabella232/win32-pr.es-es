---
description: 'Más información acerca de: limitaciones del modelo de scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitaciones del modelo de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666497"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="27a56-103">Limitaciones del modelo de scripting</span><span class="sxs-lookup"><span data-stu-id="27a56-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="27a56-104">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="27a56-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="27a56-105">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="27a56-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="27a56-106">El modelo de scripting de adquisición de imágenes de Windows (WIA) expone un subconjunto de la funcionalidad de WIA.</span><span class="sxs-lookup"><span data-stu-id="27a56-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="27a56-107">En la tabla siguiente se proporcionan descripciones de las limitaciones del modelo de scripting.</span><span class="sxs-lookup"><span data-stu-id="27a56-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="27a56-108">Funcionalidad WIA</span><span class="sxs-lookup"><span data-stu-id="27a56-108">WIA Functionality</span></span>               | <span data-ttu-id="27a56-109">Restricción del modelo de scripting</span><span class="sxs-lookup"><span data-stu-id="27a56-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a56-110">Supresión de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="27a56-110">Suppressing the user interface</span></span>  | <span data-ttu-id="27a56-111">No se puede suprimir la interfaz de usuario para establecer las propiedades de dispositivo/transferencia.</span><span class="sxs-lookup"><span data-stu-id="27a56-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="27a56-112">Configurar propiedades</span><span class="sxs-lookup"><span data-stu-id="27a56-112">Setting properties</span></span>              | <span data-ttu-id="27a56-113">No se puede establecer (escribir) ninguna propiedad de dispositivo o elemento.</span><span class="sxs-lookup"><span data-stu-id="27a56-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="27a56-114">Registrar eventos de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="27a56-114">Registering for callback events</span></span> | <span data-ttu-id="27a56-115">Solo puede recibir notificaciones para tres eventos especificados: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)y [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="27a56-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="27a56-116">Control de errores</span><span class="sxs-lookup"><span data-stu-id="27a56-116">Handling errors</span></span>                 | <span data-ttu-id="27a56-117">No se pueden controlar los errores de WIA.</span><span class="sxs-lookup"><span data-stu-id="27a56-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
