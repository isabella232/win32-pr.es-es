---
title: Detección de Media Player de Windows desde una aplicación
description: Detección de Media Player de Windows desde una aplicación
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, detectar desde aplicaciones
- detección de Media Player de Windows desde aplicaciones
- registro, detección de Media Player de Windows desde aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695450"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="c0dbd-106">Detección de Media Player de Windows desde una aplicación</span><span class="sxs-lookup"><span data-stu-id="c0dbd-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="c0dbd-107">Puede determinar qué versión de Windows Media Player está instalada mediante la comprobación de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="c0dbd-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="c0dbd-108">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Active Setup \\ componentes instalados**</span><span class="sxs-lookup"><span data-stu-id="c0dbd-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="c0dbd-109">Para Windows Media Player 6,4, consulte la clave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span><span class="sxs-lookup"><span data-stu-id="c0dbd-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="c0dbd-110">En Windows Media Player 7 o versiones posteriores, consulte la clave **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.</span><span class="sxs-lookup"><span data-stu-id="c0dbd-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="c0dbd-111">En cualquiera de estas claves, si el **IsInstalled**</span><span class="sxs-lookup"><span data-stu-id="c0dbd-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="c0dbd-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c0dbd-112">Data type</span></span>
</dt> <dd><span data-ttu-id="c0dbd-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="c0dbd-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="c0dbd-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c0dbd-114">Data type</span></span>
</dt> <dd><span data-ttu-id="c0dbd-115">string</span><span class="sxs-lookup"><span data-stu-id="c0dbd-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="c0dbd-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0dbd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0dbd-117">**Redistribuir el software de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c0dbd-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




