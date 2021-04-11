---
title: Trabajar con plantillas de cumplimiento de dispositivos
description: Trabajar con plantillas de cumplimiento de dispositivos
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- perfiles, plantillas de conformidad de dispositivos
- perfiles, plantillas de cumplimiento
- códecs, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad
- plantillas de conformidad de dispositivos, acerca de
- plantillas de conformidad
- plantillas, plantillas de conformidad de dispositivos
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149078"
---
# <a name="working-with-device-conformance-templates"></a>Trabajar con plantillas de cumplimiento de dispositivos

Debido a la gran flexibilidad de los archivos ASF, a menudo es difícil determinar si un archivo es adecuado para la reproducción en un dispositivo específico. Por ejemplo, los archivos escritos para la reproducción local en equipos de escritorio no son óptimos para su uso en dispositivos de mano. Las plantillas de conformidad de dispositivos permiten a las aplicaciones identificar rápidamente el tipo de dispositivo de reproducción para el que se diseñó un archivo. Si la plantilla de conformidad del dispositivo no coincide con el dispositivo, la aplicación puede informar al usuario de que el archivo no es apropiado para el dispositivo. De esta manera, el usuario puede estar seguro de una mejor experiencia de reproducción.

Si está escribiendo archivos exclusivamente para su uso en equipos personales, las plantillas de conformidad de dispositivos no serán la gran parte de un factor en la creación de perfiles. El propósito principal de estas plantillas es asegurarse de que los archivos creados para su uso con hardware especial son compatibles con una amplia gama de dispositivos y no solo un dispositivo.

Una plantilla de conformidad de dispositivos es una aserción de que un archivo ASF contiene datos codificados en determinados parámetros. Para obtener más información sobre la configuración adecuada para las plantillas individuales, consulte parámetros de la [plantilla de cumplimiento de dispositivos](device-conformance-template-parameters.md).

Los códecs siguientes son compatibles con las plantillas de conformidad de dispositivos:

-   Windows Media Video 9
-   Windows Media Audio 9 y versiones posteriores
-   Windows Media Audio 9 Professional y versiones posteriores
-   Windows Media Audio 9 Voice

No es necesario realizar ningún paso especial para usar las plantillas de cumplimiento de dispositivos. El códec escribe automáticamente una cadena de plantilla para cada secuencia adecuada en el archivo. El códec decidirá qué plantilla se debe usar, en función de los valores de configuración de la secuencia en el perfil. Hay cierta superposición en los parámetros de la plantilla de conformidad del dispositivo, por lo que puede que desee solicitar una plantilla específica en lugar de permitir que el códec le asigne una. Puede especificar la plantilla que desee estableciendo la \_ propiedad g wszDecoderComplexityRequested con los métodos de la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de secuencia adecuado.

Cuando se escribe un archivo ASF, la plantilla de conformidad del dispositivo real para cada flujo se establece en el valor pasado al escritor por el códec. Al abrir un archivo para leerlo, puede averiguar a qué plantilla se ajustan las secuencias del archivo mediante el uso de los métodos de la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para recuperar el \_ atributo de nivel de secuencia g wszDeviceConformanceTemplate. Para obtener más información sobre los atributos, vea [trabajar con metadatos](working-with-metadata.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Diseñar perfiles**](designing-profiles.md)
</dt> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




