---
description: Compatibilidad de plataforma y disponibilidad de códecs
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Compatibilidad de plataforma y disponibilidad de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278181"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="a8e3e-103">Compatibilidad de plataforma y disponibilidad de códecs</span><span class="sxs-lookup"><span data-stu-id="a8e3e-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="a8e3e-104">Microsoft recomienda que los proveedores de cámaras incluyan códecs de componentes de imágenes de Windows (WIC) sin procesar actualizados en la distribución de software con nuevas cámaras y que el códec actualizado se instale con la instalación de software de proveedor predeterminada Windows 7, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a8e3e-105">Los proveedores de cámaras también deben proporcionar el códec WIC más reciente como descarga de sus sitios de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="a8e3e-106">Detección de códecs</span><span class="sxs-lookup"><span data-stu-id="a8e3e-106">Codec Discovery</span></span>

<span data-ttu-id="a8e3e-107">Microsoft está haciendo lo siguiente para ayudar a los usuarios a dirigirse a los sitios web de los proveedores para descargar códecs:</span><span class="sxs-lookup"><span data-stu-id="a8e3e-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="a8e3e-108">En el explorador de Windows, si un usuario hace doble clic en un archivo que no se reconoce (el caso predeterminado en el que un archivo sin formato está en el equipo, pero el códec todavía no está instalado), un cuadro de diálogo informa de que el archivo no se reconoce y pregunta si el usuario desea encontrar un programa que entienda el archivo.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="a8e3e-109">Microsoft mantiene un servicio de redireccionamiento existente para reenviar a los usuarios a sitios web de los proveedores que pueden proporcionar el programa para comprender el archivo.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="a8e3e-110">Esta instalación existe en Windows XP y en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="a8e3e-111">La Galería fotográfica de Windows, la Galería fotográfica de Windows Live y el visor de fotografías de Windows 7 reconocen un conjunto de extensiones de archivo como archivos sin formato.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="a8e3e-112">Si los archivos de ese conjunto se encuentran en carpetas que cualquiera de estas aplicaciones están examinando y no hay instalado un códec para el archivo, se mostrará un cuadro de diálogo, tal como se describe en el párrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="a8e3e-113">Para obtener más información acerca de la detección de códecs, consulte compatibilidad con códecs y plataforma.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="a8e3e-114">Compatibilidad con la plataforma Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8e3e-114">Windows XP Platform Support</span></span>

<span data-ttu-id="a8e3e-115">Microsoft ha lanzado Windows XP SP3 con WIC y un instalador de WIC independiente para Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="a8e3e-116">Estos usan códecs WIC para habilitar la compatibilidad con miniaturas y vistas previas en esas plataformas.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="a8e3e-117">Por lo tanto, es importante que la descarga e instalación de códecs se admita y pruebe en Windows 7, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8e3e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8e3e-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a8e3e-119">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a8e3e-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8e3e-120">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="a8e3e-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="a8e3e-121">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="a8e3e-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="a8e3e-122">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="a8e3e-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



