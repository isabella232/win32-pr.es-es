---
description: En esta sección se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea Guía de programación de Media Foundation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitectura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721349"
---
# <a name="media-foundation-architecture"></a>Arquitectura de Media Foundation

En esta sección se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea [Guía de programación de Media Foundation](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                         | Descripción                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general de la arquitectura de Media Foundation](overview-of-the-media-foundation-architecture.md)<br/> | Proporciona información general de alto nivel sobre la arquitectura de Media Foundation.<br/>                                                                                                                                                                                                               |
| [Media Foundation primitivas](media-foundation-primitives.md)<br/>                                     | Describe algunas interfaces básicas que se usan en Media Foundation.<br/> Casi todas las aplicaciones Media Foundation usarán estas interfaces.<br/>                                                                                                                       |
| [API de Media Foundation Platform](media-foundation-platform-apis.md)<br/>                               | Describe las funciones básicas de Media Foundation, como las devoluciones de llamada asincrónicas y las colas de trabajos.<br/> Algunas aplicaciones pueden usar interfaces de nivel de plataforma. Además, los complementos personalizados, como los orígenes multimedia y MFTs, usan estas interfaces.<br/>                                       |
| [Canalización de Media Foundation](media-foundation-pipeline.md)<br/>                                         | La capa de canalización Media Foundation se compone de orígenes de medios, MFTs y receptores de medios. La mayoría de las aplicaciones no llaman a métodos directamente en la capa de canalización. En su lugar, las aplicaciones usan uno de los niveles superiores, como la sesión multimedia o el lector de origen y el escritor del receptor.<br/> |
| [Sesión de medios](media-session.md)<br/>                                                                 | La sesión multimedia administra el flujo de datos en la canalización de Media Foundation.<br/>                                                                                                                                                                                                           |
| [Lector de origen](source-reader.md)<br/>                                                                 | El lector de origen permite a una aplicación obtener datos de un origen multimedia, sin necesidad de realizar llamadas directamente a las API de origen multimedia. El lector de origen también puede realizar la descodificación de secuencias comprimidas.<br/>                                                            |
| [Ruta de acceso a medios protegidos](protected-media-path.md)<br/>                                                   | La ruta de acceso a medios protegidos (PMP) proporciona un entorno protegido para reproducir contenido de vídeo Premium. No es necesario usar el PMP al escribir una aplicación Media Foundation. <br/>                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation y COM](media-foundation-and-com.md)
</dt> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




