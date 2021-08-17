---
description: Perfil de modo restringido y establecimiento de configuración
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Perfil de modo restringido y establecimiento de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747055"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Perfil de modo restringido y establecimiento de configuración

Debido a la variedad de tipos de datos que se pueden descodificar mediante DirectX VA, y las múltiples configuraciones de descodificación admitidas en DirectX VA para cada uno de estos tipos de datos (por ejemplo, el uso de búferes de secuencia de bits frente a la descodificación de diferencia residual del host frente al IDCT basado en acelerador con y sin cifrado de cada tipo de búfer pertinente, y así sucesivamente),  Creemos que sería poco sencillo especificar simplemente un GUID único para cada tipo de datos único y la configuración de lacoding. Esto crearía un gran número de GUID (por ejemplo, hipotéticamente si hubiera 16 perfiles de DIRECTX VA y 16 configuraciones posibles para cada uno, tendría que haber 256 GUID definidos, lo que requeriría 4 kilobytes de memoria solo para contener todos ellos. Este problema es la parte más difícil de determinar cómo asignar DirectX VA a **IAMVideoAccelerator,** y el resto de la definición operativa es bastante sencillo. Como resultado, se especifica un GUID único solo para cada tipo de datos (para cada perfil de modo restringido) y se permite asociar un GUID adicional a cada tipo de cifrado. A continuación, la configuración de descodificación se establece entre el descodificador y el acelerador mediante una negociación subordinada de nivel inferior mediante operaciones de sondeo y bloqueo para establecer configuraciones para cada tipo de función va de DirectX.

 

 



