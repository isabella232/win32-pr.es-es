---
description: El componente de creación de imágenes de Windows (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introducción (cómo escribir un códec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716134"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="0e895-103">Introducción (cómo escribir un códec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="0e895-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="0e895-104">El componente de creación de imágenes de Windows (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e895-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="0e895-105">WIC también está disponible en Windows XP y Windows Server 2003, ya sea como parte de Microsoft .NET Framework 3,0 o como un componente independiente que se puede redistribuir.</span><span class="sxs-lookup"><span data-stu-id="0e895-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="0e895-106">Cualquier aplicación que use WIC puede tener acceso, mostrar, procesar e imprimir imágenes en cualquier formato de imagen que proporcione un códec habilitado para WIC, mediante un único conjunto de interfaces coherentes que eliminan la necesidad de tener conocimientos especializados de formatos específicos.</span><span class="sxs-lookup"><span data-stu-id="0e895-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="0e895-107">El explorador de Windows Vista, la Galería fotográfica de Windows Vista, la Galería fotográfica de Windows y el visor de fotografías de Windows 7 se basan en WIC.</span><span class="sxs-lookup"><span data-stu-id="0e895-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="0e895-108">Después de instalar un códec habilitado para WIC en un sistema Windows Vista o Windows 7, el sistema operativo proporciona el mismo nivel de compatibilidad con el formato de imagen asociado que para los formatos de imagen estándar que se distribuyen con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0e895-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="0e895-109">Dado que escribe el códec para su propio formato de imagen, puede garantizar una calidad coherente en cualquier lugar donde se use el formato de la imagen y obtener las ventajas de la compatibilidad total con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0e895-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e895-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e895-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0e895-111">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0e895-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e895-112">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0e895-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0e895-113">Cómo funciona el componente de creación de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="0e895-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="0e895-114">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0e895-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="0e895-115">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="0e895-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



