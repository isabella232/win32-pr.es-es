---
description: Uso del perfil avanzado de Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del perfil avanzado de Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689632"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="ee139-103">Uso del perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="ee139-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="ee139-104">Los procedimientos de vídeo básicos que se describen en la sección [trabajar con vídeo](workingwithvideo.md) también se aplican directamente al perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="ee139-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="ee139-105">No se requiere ningún procedimiento especial.</span><span class="sxs-lookup"><span data-stu-id="ee139-105">No special procedures are required.</span></span>

<span data-ttu-id="ee139-106">El perfil avanzado de Windows Media Video 9 está asociado a los identificadores de clase CLSID \_ CWMV9EncMediaObject y CLSID \_ CWMVDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="ee139-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="ee139-107">El valor FOURCC para los tipos de medios que usan este códec es "WVC1".</span><span class="sxs-lookup"><span data-stu-id="ee139-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="ee139-108">El perfil avanzado de Windows Media Video 9 es compatible con todos los modos de codificación comunes, como la codificación entrelazada, la codificación entrelazada y progresiva mixta, las resoluciones que son diferentes de las que se muestran y las características de reducción del intervalo.</span><span class="sxs-lookup"><span data-stu-id="ee139-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="ee139-109">Otra característica es la capacidad de almacenar metadatos de secuencia y fotogramas en el propio flujo de bits; anteriormente, este tenía el uso de la API de extensiones de unidad de datos y ASF.</span><span class="sxs-lookup"><span data-stu-id="ee139-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="ee139-110">Las siguientes propiedades del perfil avanzado de Windows Media Video 9, que se puede controlar mediante la configuración del registro, no tienen las cadenas **IPropertyBag** o **IPropertyStore** correspondientes:</span><span class="sxs-lookup"><span data-stu-id="ee139-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="ee139-111">Opción Dquant.</span><span class="sxs-lookup"><span data-stu-id="ee139-111">Dquant Option.</span></span>
-   <span data-ttu-id="ee139-112">Dquant.</span><span class="sxs-lookup"><span data-stu-id="ee139-112">Dquant Strength.</span></span>
-   <span data-ttu-id="ee139-113">Forzar la superposición.</span><span class="sxs-lookup"><span data-stu-id="ee139-113">Force Overlap.</span></span>
-   <span data-ttu-id="ee139-114">Método de costo del vector de movimiento.</span><span class="sxs-lookup"><span data-stu-id="ee139-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="ee139-115">Obtención de una calidad visual óptima</span><span class="sxs-lookup"><span data-stu-id="ee139-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="ee139-116">Para la mayoría de los datos de vídeo, para lograr una calidad visual óptima mediante el perfil avanzado de Windows Media Video 9, puede establecer la propiedad [ \_ COMPRESSIONOPTIMIZATIONTYPE de MFPKEY](mfpkey-compressionoptimizationtypeproperty.md) en 1.</span><span class="sxs-lookup"><span data-stu-id="ee139-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="ee139-117">Acerca de los códecs de perfil avanzado de Windows Media Video 9 anteriores</span><span class="sxs-lookup"><span data-stu-id="ee139-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="ee139-118">La versión actual del códec de perfil avanzado de Windows Media Video 9 se basa en la sociedad del estándar de ingeniería de películas y televisión (SMPTE) para el perfil avanzado VC-1 (SMPTE 421M).</span><span class="sxs-lookup"><span data-stu-id="ee139-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="ee139-119">Este códec reemplaza el códec anterior de Windows también llamado códec de perfil avanzado de Windows Media Video 9 que se identificó mediante el código FOURCC "WMVA".</span><span class="sxs-lookup"><span data-stu-id="ee139-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="ee139-120">La versión anterior del códec VC-1 se implementó antes de finalizar el estándar de perfil avanzado de VC-1 y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="ee139-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee139-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee139-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee139-122">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="ee139-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="ee139-123">Uso de la configuración avanzada del códec de perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="ee139-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



