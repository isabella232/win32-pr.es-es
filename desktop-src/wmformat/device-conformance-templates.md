---
title: Plantillas de conformidad de dispositivos
description: Plantillas de conformidad de dispositivos
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad de dispositivos
- plantillas de conformidad de dispositivos, acerca de
- templates,device conformance templates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eea2bcb923cef2a92519b613f22bab046fbde9a50cbbdf29f22a0921a56fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655676"
---
# <a name="device-conformance-templates"></a>Plantillas de conformidad de dispositivos

Los códecs Windows serie Media 9 admiten plantillas de conformidad de dispositivos, que son intervalos definidos de valores de configuración de flujo y algoritmos de códec. Cada plantilla define los intervalos de valores adecuados para determinados dispositivos.

En el pasado, los fabricantes de hardware que hacían que los dispositivos fueran capaces de reproducir archivos ASF funcionaban según sus propios estándares. Esto dio lugar a una amplia gama de funcionalidades en dispositivos similares que continúa hoy en día.

Con las plantillas de conformidad de dispositivos, los códecs Windows media establecen un terreno común para dispositivos similares. Los fabricantes de hardware pueden especificar las plantillas a las que se ajustan sus dispositivos, lo que permite a los creadores de contenido dirigir sus archivos a dispositivos de lectura con mayor confianza. También es más fácil para las aplicaciones de reproductor determinar si un archivo es inadecuado para el dispositivo antes de intentar reproducirlo.

Una plantilla de conformidad de dispositivo se identifica mediante una cadena, que se almacena como un atributo de metadatos asociado a la secuencia a la que se aplica la plantilla. Para obtener una lista de las plantillas y sus cadenas y parámetros, consulte [Device Conformance Template Parameters](device-conformance-template-parameters.md).

Las plantillas de conformidad de dispositivos se admiten para todos los códecs de la serie Windows Media 9 y versiones posteriores, excepto el códec de pantalla Windows Media Video 9 y el códec sin pérdida de Windows Media Audio 9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Trabajar con plantillas de conformidad de dispositivos**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




