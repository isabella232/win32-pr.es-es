---
description: En esta sección se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea Media Foundation Programming Guide.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitectura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974224"
---
# <a name="media-foundation-architecture"></a>Arquitectura de Media Foundation

En esta sección se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre cómo usar Media Foundation tareas de programación específicas, [vea Media Foundation Programming Guide](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                         | Descripción                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a la arquitectura Media Foundation de datos](overview-of-the-media-foundation-architecture.md)<br/> | Proporciona información general sobre la arquitectura de Media Foundation.<br/>                                                                                                                                                                                                               |
| [Media Foundation primitivos](media-foundation-primitives.md)<br/>                                     | Describe algunas interfaces básicas que se usan en Media Foundation.<br/> Casi todas Media Foundation aplicaciones usarán estas interfaces.<br/>                                                                                                                       |
| [Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)<br/>                               | Describe las funciones Media Foundation principales, como las devoluciones de llamada asincrónicas y las colas de trabajo.<br/> Algunas aplicaciones pueden usar interfaces de nivel de plataforma. Además, los complementos personalizados, como los orígenes multimedia y las MTA, usan estas interfaces.<br/>                                       |
| [Media Foundation canalización](media-foundation-pipeline.md)<br/>                                         | La Media Foundation de canalización consta de orígenes multimedia, MTA y receptores multimedia. La mayoría de las aplicaciones no llaman a métodos directamente en el nivel de canalización. En su lugar, las aplicaciones usan una de las capas superiores, como la sesión multimedia o el lector de origen y el escritor de receptores.<br/> |
| [Sesión multimedia](media-session.md)<br/>                                                                 | La sesión multimedia administra el flujo de datos en la Media Foundation datos.<br/>                                                                                                                                                                                                           |
| [Lector de origen](source-reader.md)<br/>                                                                 | El Lector de origen permite que una aplicación obtenga datos de un origen multimedia, sin necesidad de llamar directamente a las API de origen multimedia. El Lector de origen también puede realizar la decodificación de secuencias comprimidas.<br/>                                                            |
| [Ruta de acceso multimedia protegida](protected-media-path.md)<br/>                                                   | La ruta de acceso multimedia protegida (PMP) proporciona un entorno protegido para reproducir contenido de vídeo premium. No es necesario usar el PMP al escribir una Media Foundation aplicación. <br/>                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation y COM](media-foundation-and-com.md)
</dt> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 




