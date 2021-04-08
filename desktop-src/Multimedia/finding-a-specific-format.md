---
title: Buscar un formato específico
description: Buscar un formato específico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Administrador de compresión de audio (ACM), buscar formatos
- ACM (Administrador de compresión de audio), buscar formatos
- Ejemplos de ACM, buscar formatos
- buscar formatos
- acmFormatEnum función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994495"
---
# <a name="finding-a-specific-format"></a><span data-ttu-id="3c568-108">Buscar un formato específico</span><span class="sxs-lookup"><span data-stu-id="3c568-108">Finding a Specific Format</span></span>

<span data-ttu-id="3c568-109">Una aplicación podría tener solo una especificación parcial para un formato cuando necesita la especificación completa.</span><span class="sxs-lookup"><span data-stu-id="3c568-109">An application might have only a partial specification for a format when it needs the full specification.</span></span> <span data-ttu-id="3c568-110">Por ejemplo, la especificación podría estipular un formato ADPCM mono de 4 bits de 11 kHz, pero no el promedio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3c568-110">For example, the specification might stipulate an 11-kHz mono, 4-bit ADPCM format, but not the average bytes per second.</span></span> <span data-ttu-id="3c568-111">La aplicación puede obtener el formato completo sin la intervención del usuario mediante la función [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) y especificando marcas en el parámetro *fdwEnum* .</span><span class="sxs-lookup"><span data-stu-id="3c568-111">The application can get the full format without user intervention by using the [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) function and specifying flags in the *fdwEnum* parameter.</span></span>

 

 




