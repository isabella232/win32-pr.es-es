---
description: Introducción (instrucciones WIC para formatos de imagen RAW de cámara)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introducción (instrucciones WIC para formatos de imagen RAW de cámara)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278178"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="64dc8-103">Introducción (instrucciones WIC para formatos de imagen RAW de cámara)</span><span class="sxs-lookup"><span data-stu-id="64dc8-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="64dc8-104">El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes.</span><span class="sxs-lookup"><span data-stu-id="64dc8-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="64dc8-105">WIC permite que los proveedores de software y hardware desarrollen códecs para que sus propios formatos de imagen puedan obtener la misma compatibilidad de plataforma que los formatos de imagen nativa, como el formato de archivo de imagen etiquetado (TIFF), el grupo de expertos fotográficos (JPEG) o la foto HD.</span><span class="sxs-lookup"><span data-stu-id="64dc8-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="64dc8-106">WIC proporciona un conjunto único y coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="64dc8-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="64dc8-107">Por lo tanto, cualquier aplicación que use WIC recibirá compatibilidad automática con los nuevos formatos de imagen en cuanto se instale el códec.</span><span class="sxs-lookup"><span data-stu-id="64dc8-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="64dc8-108">WIC también proporciona un marco de metadatos extensible que permite que las aplicaciones lean y escriban sus propios metadatos de propiedad directamente en archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.</span><span class="sxs-lookup"><span data-stu-id="64dc8-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="64dc8-109">WIC se incluye con Windows Presentation Foundation (WPF) y está integrado en Windows Vista y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="64dc8-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="64dc8-110">También está disponible como componente redistribuible independiente para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64dc8-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="64dc8-111">Estas instrucciones están diseñadas para ayudar a los fabricantes de formatos sin formato en su desarrollo de códecs WIC.</span><span class="sxs-lookup"><span data-stu-id="64dc8-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64dc8-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64dc8-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64dc8-113">**Vista**</span><span class="sxs-lookup"><span data-stu-id="64dc8-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64dc8-114">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="64dc8-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="64dc8-115">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="64dc8-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="64dc8-116">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="64dc8-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



