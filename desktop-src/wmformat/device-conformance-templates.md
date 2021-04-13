---
title: Plantillas de conformidad de dispositivos
description: Plantillas de conformidad de dispositivos
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad de dispositivos
- plantillas de conformidad de dispositivos, acerca de
- plantillas, plantillas de conformidad de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357685"
---
# <a name="device-conformance-templates"></a>Plantillas de conformidad de dispositivos

Los códecs de Windows Media 9 Series admiten plantillas de conformidad de dispositivos, que son intervalos definidos de valores de configuración de secuencia y algoritmos de códecs. Cada plantilla define los intervalos de valores adecuados para determinados dispositivos.

En el pasado, los fabricantes de hardware que hacían que los dispositivos capaces de reproducir archivos ASF estaban trabajando con sus propios estándares. Como resultado, la gama de funcionalidades es muy dispares en dispositivos similares que continúan hoy en día.

Con las plantillas de conformidad de dispositivos, los códecs de Windows Media establecen una base común para dispositivos similares. Los fabricantes de hardware pueden indicar las plantillas a las que se ajustan los dispositivos, lo que permite a los creadores de contenido destinar con mayor seguridad sus archivos a los dispositivos de lectura. También es más fácil que las aplicaciones de reproducción determinen si un archivo no es apropiado para el dispositivo antes de intentar reproducirlo.

Una plantilla de conformidad de dispositivos se identifica mediante una cadena, que se almacena como un atributo de metadatos asociado con la secuencia a la que se aplica la plantilla. Para obtener una lista de las plantillas y sus cadenas y parámetros, vea parámetros de la [plantilla de conformidad de dispositivos](device-conformance-template-parameters.md).

Las plantillas de conformidad de dispositivos se admiten para todos los códecs de la serie Windows Media 9 y posteriores, excepto el códec de pantalla de Windows Media Video 9 y el códec Windows Media Audio 9 Lossless.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Trabajar con plantillas de cumplimiento de dispositivos**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




