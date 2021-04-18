---
description: Los especificadores de tipo de dispositivo de adquisición de imágenes de Windows (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715179"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="bd972-103">Especificadores de tipo de dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="bd972-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="bd972-104">Los especificadores de tipo de dispositivo de adquisición de imágenes de Windows (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="bd972-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="bd972-105">Use la \_ macro Get STIDEVICE \_ Type para obtener estos valores de la propiedad de tipo de dispositivo WIA.</span><span class="sxs-lookup"><span data-stu-id="bd972-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="bd972-106">Los siguientes son especificadores de tipo de dispositivo WIA válidos:</span><span class="sxs-lookup"><span data-stu-id="bd972-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="bd972-107">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="bd972-107">Device Type</span></span>                 | <span data-ttu-id="bd972-108">Significado</span><span class="sxs-lookup"><span data-stu-id="bd972-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd972-109">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="bd972-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="bd972-110">Dispositivo WIA genérico.</span><span class="sxs-lookup"><span data-stu-id="bd972-110">Generic WIA device.</span></span> <span data-ttu-id="bd972-111">Durante las enumeraciones de dispositivos, esta constante se usa para enumerar todos los dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="bd972-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="bd972-112">StiDeviceTypeDigitalCamera</span><span class="sxs-lookup"><span data-stu-id="bd972-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="bd972-113">El dispositivo es una cámara.</span><span class="sxs-lookup"><span data-stu-id="bd972-113">The device is a camera.</span></span> <span data-ttu-id="bd972-114">*Este especificador no es compatible con* . Windows Vista *y versiones posteriores.*</span><span class="sxs-lookup"><span data-stu-id="bd972-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="bd972-115">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="bd972-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="bd972-116">El dispositivo es un escáner.</span><span class="sxs-lookup"><span data-stu-id="bd972-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="bd972-117">StiDeviceTypeStreamingVideo</span><span class="sxs-lookup"><span data-stu-id="bd972-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="bd972-118">El dispositivo contiene vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="bd972-118">The device contains streaming video.</span></span> <span data-ttu-id="bd972-119">*Este especificador no es compatible con* . Windows Server 2003 *,* Windows Vista *o posterior.*</span><span class="sxs-lookup"><span data-stu-id="bd972-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



