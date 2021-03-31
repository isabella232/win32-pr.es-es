---
title: Generar un formato no estándar
description: Generar un formato no estándar
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Administrador de compresión de audio (ACM), formatos no estándar
- ACM (Administrador de compresión de audio), formatos no estándar
- Ejemplos de ACM, formatos no estándar
- acmFormatSuggest función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903426"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="4c7f3-107">Generar un formato no estándar</span><span class="sxs-lookup"><span data-stu-id="4c7f3-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="4c7f3-108">A veces, una aplicación necesita un formato no estándar.</span><span class="sxs-lookup"><span data-stu-id="4c7f3-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="4c7f3-109">Por ejemplo, una aplicación podría necesitar un archivo de formato ADPCM de 16 kHz.</span><span class="sxs-lookup"><span data-stu-id="4c7f3-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="4c7f3-110">Dado que 16 kHz no es estándar, las funciones de enumeración no generarán este formato.</span><span class="sxs-lookup"><span data-stu-id="4c7f3-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="4c7f3-111">De hecho, a partir de la codificación personalizada de los algoritmos de formato en la aplicación, no hay ninguna manera confiable de generar un formato no estándar.</span><span class="sxs-lookup"><span data-stu-id="4c7f3-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="4c7f3-112">Sin embargo, a veces es posible generar un formato análogo mediante la configuración de un formato PCM válido con toda la información necesaria y, a continuación, mediante la función [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) .</span><span class="sxs-lookup"><span data-stu-id="4c7f3-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="4c7f3-113">Dado que los compresores y descompresores intentan sugerir un formato más cercano al formato deseado, normalmente se conserva el número de canales y la frecuencia.</span><span class="sxs-lookup"><span data-stu-id="4c7f3-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




