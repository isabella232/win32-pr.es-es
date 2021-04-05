---
title: Secuencias Web
description: Secuencias Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- SDK de Windows Media Format, secuencias Web
- Advanced Systems Format (ASF), streams Web
- ASF (formato de sistemas avanzados), secuencias Web
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- Secuencias Web, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075651"
---
# <a name="web-streams"></a>Secuencias Web

Una secuencia web es como una secuencia de archivos en que contiene archivos de datos. En una secuencia Web, estos archivos suelen ser páginas HTML y gráficos asociados en formato GIF o JPEG.

Las secuencias Web pueden ser especialmente útiles para los archivos ASF que se usan como presentaciones. Antes de la compatibilidad de las secuencias Web, las presentaciones tendrían direcciones URL en secuencias de scripts dentro de un archivo para que una página web se cargara en un tiempo predeterminado. La dificultad era que la congestión de la red podría provocar retrasos y crear una experiencia de visualización deficiente.

Con las secuencias Web, las partes constituyentes de las páginas web pueden incluirse en el archivo ASF como una secuencia. A medida que se reciben los archivos, se pueden almacenar en caché para que, cuando el comando para mostrar (o representar) una dirección URL se entregue, se pueda acceder al instante mediante un explorador. Esto permite una reproducción fluida y coherente. El comando Render se entrega en la propia secuencia Web, no como un comando de script en una secuencia independiente.

Se recomienda que las secuencias web creadas con el SDK de Windows Media Format 9 series o posterior se les proporcione el número de versión 1. Este valor se especifica en la estructura de [**\_ \_ formato de Webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) en el miembro **wVersion** . El propio SDK no hace nada para aplicar esta versión.

> [!Note]  
> Al conectarse a secuencias de difusión en directo que tienen secuencias Web, es posible que el usuario reciba un comando de representación antes de que el archivo especificado se encuentra realmente en la caché local. A menos que la aplicación controle esta condición, el explorador mostrará el error "página no encontrada".

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos arbitrarios**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de secuencias Web**](configuring-web-streams.md)
</dt> </dl>

 

 




