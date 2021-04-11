---
title: Configurar secuencias de scripts
description: Configurar secuencias de scripts
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flujos, configurar secuencias de scripts
- códecs, configurar secuencias de scripts
- secuencias de comandos, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075595"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="75fb2-106">Configurar secuencias de scripts</span><span class="sxs-lookup"><span data-stu-id="75fb2-106">Configuring Script Streams</span></span>

<span data-ttu-id="75fb2-107">Al igual que todos los tipos de secuencia arbitrarios, los flujos de scripts deben tener una ventana de velocidad de bits y de búfer definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="75fb2-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="75fb2-108">El tipo de medio principal de la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) debe establecerse en el script WMMEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="75fb2-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="75fb2-109">Los flujos de scripts deben tener el miembro **formatType** de **tipo de \_ medio \_ de WM** establecido en el \_ script WMFORMAT, lo que indica que el miembro **pbFormat** apunta a una estructura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .</span><span class="sxs-lookup"><span data-stu-id="75fb2-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="75fb2-110">Solo hay un tipo de script admitido, WMSCRIPTTYPE \_ TwoStrings.</span><span class="sxs-lookup"><span data-stu-id="75fb2-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75fb2-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75fb2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75fb2-112">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="75fb2-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="75fb2-113">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="75fb2-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="75fb2-114">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="75fb2-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




