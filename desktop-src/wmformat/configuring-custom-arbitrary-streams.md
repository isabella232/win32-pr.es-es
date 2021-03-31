---
title: Configuración de secuencias arbitrarias personalizadas
description: Configuración de secuencias arbitrarias personalizadas
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flujos, configurar secuencias arbitrarias personalizadas
- códecs, configurar secuencias arbitrarias personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775697"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configuración de secuencias arbitrarias personalizadas

Al usar su propio tipo de datos arbitrario, debe crear un valor de GUID para que sirva como el identificador de tipo de medio principal para él. Cuando el escritor encuentra una secuencia en un perfil con un tipo principal que no reconoce, se supone que la secuencia son datos arbitrarios personalizados. Aceptará sus ejemplos, los pondrá en paquetes y los combinará con ejemplos de las otras secuencias del archivo sin comprobar de ningún modo los datos.

También puede crear sus propios identificadores GUID de subtipos para definir subcategorías de los datos personalizados. El escritor omitirá todos estos subtipos por completo, pero se conservarán en la sección de encabezado del archivo ASF, de modo que la aplicación de lectura pueda recuperarlos y tomar decisiones basadas en ellos.

Una secuencia arbitraria requiere una ventana de velocidad de bits y de búfer, y debe tener una estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con los valores borrados, excepto el tipo de medio principal y el subtipo (si se usa uno).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flujos de datos arbitrarios personalizados**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




