---
description: Formatos de imagen sin procesar en Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagen sin procesar en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278179"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="56f82-103">Formatos de imagen sin procesar en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56f82-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="56f82-104">El explorador de Windows Vista, la Galería fotográfica de Windows Vista, la Galería fotográfica de Windows Live y el visor de fotos de Windows 7 usan Windows Imaging Component (WIC) y, por lo tanto, admiten formatos de imagen sin procesar cuando se instalan los códecs adecuados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="56f82-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="56f82-105">Dado que WIC es una arquitectura de creación de imágenes extensible, cualquier aplicación WIC puede consumir nuevos formatos de imagen en cuanto se instalan nuevos códecs en el sistema.</span><span class="sxs-lookup"><span data-stu-id="56f82-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="56f82-106">Esto hace que WIC sea idóneo como una solución Plug and Play para los formatos de imagen sin procesar que producen las cámaras digitales.</span><span class="sxs-lookup"><span data-stu-id="56f82-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="56f82-107">A través de WIC, las aplicaciones de Windows pueden obtener soporte técnico para los nuevos modelos de cámara cada vez que estén disponibles códecs actualizados (idealmente, con nuevas cámaras).</span><span class="sxs-lookup"><span data-stu-id="56f82-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="56f82-108">Los creadores de códecs pueden admitir estos escenarios implementando interfaces WIC que son comunes a todos los tipos de imagen, como se describe más detalladamente en este documento.</span><span class="sxs-lookup"><span data-stu-id="56f82-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="56f82-109">En la actualidad, la mayoría de las aplicaciones de consumidor principales no tienen ningún conocimiento especial de los formatos de imagen sin procesar y no exponen una interfaz de usuario para ajustar la configuración de procesamiento sin procesar.</span><span class="sxs-lookup"><span data-stu-id="56f82-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="56f82-110">Sin embargo, para admitir aplicaciones de imágenes especializadas, los creadores de códecs sin formato también deben implementar la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="56f82-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="56f82-111">Esta interfaz expone características especiales para imágenes sin procesar, como la capacidad de realizar ajustes de imagen comunes y procesar (desarrollar) imágenes sin procesar en espacios de colores rojo-verde-azul (RGB) especificados.</span><span class="sxs-lookup"><span data-stu-id="56f82-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="56f82-112">Hay muchas otras interfaces WIC importantes para que los autores de códecs sin formato implementen.</span><span class="sxs-lookup"><span data-stu-id="56f82-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="56f82-113">Estos se describen con más detalle en esta serie de temas.</span><span class="sxs-lookup"><span data-stu-id="56f82-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56f82-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56f82-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="56f82-115">**Vista**</span><span class="sxs-lookup"><span data-stu-id="56f82-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="56f82-116">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="56f82-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="56f82-117">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="56f82-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="56f82-118">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="56f82-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



