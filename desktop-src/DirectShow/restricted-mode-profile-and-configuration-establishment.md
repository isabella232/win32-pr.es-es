---
description: Establecimiento de configuración y Perfil de modo restringido
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Establecimiento de configuración y Perfil de modo restringido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422854"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="b8080-103">Establecimiento de configuración y Perfil de modo restringido</span><span class="sxs-lookup"><span data-stu-id="b8080-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="b8080-104">Debido a la variedad de tipos de datos que puede descodificar con DirectX VA, además, se admiten varias configuraciones de descodificación en DirectX VA para cada uno de estos tipos de datos (por ejemplo, mediante el uso de búferes de fragmentada frente a la descodificación de diferencias residuales del host frente a IDCT basadas en el acelerador con y sin cifrado de cada tipo de búfer pertinente, etc.</span><span class="sxs-lookup"><span data-stu-id="b8080-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="b8080-105">Esto crearía un gran número de GUID (por ejemplo, subiendo si había 16 perfiles de DirectX VA y 16 configuraciones posibles para cada uno de ellos, tendría que haber 256 GUID definidos), requiriendo 4 kilobytes de memoria para contenerlos todos.</span><span class="sxs-lookup"><span data-stu-id="b8080-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="b8080-106">Este problema es la parte más difícil de determinar cómo asignar DirectX VA a **IAMVideoAccelerator**, con el resto de la definición operativa principalmente es bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="b8080-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="b8080-107">Como resultado, solo se especifica un GUID único para cada tipo de datos (para cada perfil de modo restringido) y se permite asociar un GUID adicional a cada tipo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="b8080-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="b8080-108">A continuación, se establece la configuración de descodificación entre el descodificador y el acelerador mediante una negociación subordinada de nivel inferior mediante operaciones de sondeo y bloqueo para establecer configuraciones para cada tipo de función de DirectX.</span><span class="sxs-lookup"><span data-stu-id="b8080-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



