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
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Establecimiento de configuración y Perfil de modo restringido

Debido a la variedad de tipos de datos que puede descodificar con DirectX VA, además, se admiten varias configuraciones de descodificación en DirectX VA para cada uno de estos tipos de datos (por ejemplo, mediante el uso de búferes de fragmentada frente a la descodificación de diferencias residuales del host frente a IDCT basadas en el acelerador con y sin cifrado de cada tipo de búfer pertinente, etc. Esto crearía un gran número de GUID (por ejemplo, subiendo si había 16 perfiles de DirectX VA y 16 configuraciones posibles para cada uno de ellos, tendría que haber 256 GUID definidos), requiriendo 4 kilobytes de memoria para contenerlos todos. Este problema es la parte más difícil de determinar cómo asignar DirectX VA a **IAMVideoAccelerator**, con el resto de la definición operativa principalmente es bastante sencillo. Como resultado, solo se especifica un GUID único para cada tipo de datos (para cada perfil de modo restringido) y se permite asociar un GUID adicional a cada tipo de cifrado. A continuación, se establece la configuración de descodificación entre el descodificador y el acelerador mediante una negociación subordinada de nivel inferior mediante operaciones de sondeo y bloqueo para establecer configuraciones para cada tipo de función de DirectX.

 

 



