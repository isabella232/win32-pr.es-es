---
title: Configuración de parámetros arbitrarios personalizados Secuencias
description: Configuración de parámetros arbitrarios personalizados Secuencias
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- streams,configuring custom arbitrary streams
- códecs, configurar secuencias arbitrarias personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b98b25ae9f973682ee3987ed8b590d485288e72e0b5ef7977eb7f3da0d1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809815"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configuración de parámetros arbitrarios personalizados Secuencias

Al usar su propio tipo de datos arbitrario, debe crear un valor GUID para que sirva como identificador de tipo multimedia principal para él. Cuando el escritor encuentra una secuencia en un perfil con un tipo principal que no reconoce, asume que la secuencia son datos arbitrarios personalizados. Aceptará los ejemplos, los paquetes y los combinará con ejemplos de las otras secuencias del archivo sin comprobar los datos de ninguna manera.

También puede crear sus propios identificadores GUID de subtipo para definir subcategorías de los datos personalizados. El escritor omitirá estos subtipos por completo, pero se conservarán en la sección de encabezado del archivo ASF, por lo que la aplicación de lectura puede recuperarlos y tomar decisiones basadas en ellos.

Una secuencia arbitraria requiere una velocidad de bits y una ventana de búfer, y debe tener una estructura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con los valores borrados, excepto el tipo de medio principal y el subtipo (si se usa uno).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Datos arbitrarios personalizados Secuencias**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




