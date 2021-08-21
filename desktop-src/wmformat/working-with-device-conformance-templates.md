---
title: Trabajar con plantillas de conformidad de dispositivos
description: Trabajar con plantillas de conformidad de dispositivos
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- perfiles, plantillas de conformidad de dispositivos
- perfiles, plantillas de conformidad
- códecs, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad
- plantillas de conformidad de dispositivos, acerca de
- plantillas de conformidad
- templates,device conformance templates
- Formato de sistemas avanzados (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e10bc09ccb72ae5b63894d3d7a943f377a0f45980186ab40178896425c733b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653275"
---
# <a name="working-with-device-conformance-templates"></a>Trabajar con plantillas de conformidad de dispositivos

Debido a la gran flexibilidad de los archivos ASF, a menudo es difícil determinar si un archivo es adecuado para la reproducción en un dispositivo específico. Por ejemplo, los archivos escritos para la reproducción local en equipos de escritorio no son óptimos para su uso en dispositivos portátiles. Las plantillas de conformidad de dispositivos permiten a las aplicaciones identificar rápidamente el tipo de dispositivo de reproducción para el que se ha diseñado un archivo. Si la plantilla de conformidad del dispositivo no coincide con el dispositivo, la aplicación puede informar al usuario de que el archivo no es adecuado para el dispositivo. De esta manera, el usuario puede estar seguro de una mejor experiencia de reproducción.

Si escribe archivos exclusivamente para su uso en equipos personales, las plantillas de conformidad de dispositivos no serán tan factores para crear perfiles. El propósito principal de estas plantillas es asegurarse de que los archivos creados para su uso con hardware especial son compatibles con toda una gama de dispositivos y no solo con un único dispositivo.

Una plantilla de conformidad de dispositivos es una aserción de que un archivo ASF contiene datos codificados dentro de determinados parámetros. Para obtener más información sobre la configuración adecuada para las plantillas individuales, vea [Parámetros de plantilla de conformidad de dispositivos](device-conformance-template-parameters.md).

Los códecs siguientes admiten plantillas de conformidad de dispositivos:

-   Windows Vídeo multimedia 9
-   Windows Audio multimedia 9 y versiones posteriores
-   Windows Audio multimedia 9 Professional y versiones posteriores
-   Windows Audio multimedia 9 Voz

No es necesario realizar ningún paso especial para usar plantillas de conformidad de dispositivos. El códec escribe automáticamente una cadena de plantilla para cada secuencia adecuada del archivo. El códec decidirá qué plantilla usar, en función de los valores de configuración de flujo en el perfil. Hay cierta superposición en los parámetros de plantilla de conformidad de dispositivos, por lo que es posible que desee solicitar una plantilla específica en lugar de permitir que el códec le asigne una. Puede especificar la plantilla que desea estableciendo la propiedad g wszDecoderComplexityRequested con los métodos de la interfaz \_ [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de flujo adecuado.

Cuando se escribe un archivo ASF, la plantilla de conformidad real del dispositivo para cada secuencia se establece en el valor que el códec pasa al escritor. Al abrir un archivo para lectura, puede averiguar a qué plantilla se ajustan las secuencias del archivo mediante los métodos de la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para recuperar el atributo de nivel de secuencia \_ g wszDeviceConformanceTemplate. Para obtener más información sobre los atributos, vea [Trabajar con metadatos.](working-with-metadata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Diseño de perfiles**](designing-profiles.md)
</dt> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




