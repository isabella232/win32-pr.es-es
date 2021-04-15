---
title: Detección de capacidades de formato de dispositivo
description: Detección de capacidades de formato de dispositivo
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- Administrador de dispositivos, funcionalidades del dispositivo
- Guía de programación, funcionalidades del dispositivo
- aplicaciones de escritorio, funcionalidades de dispositivo
- creación de aplicaciones de Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- escribir archivos en dispositivos, funcionalidades del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695275"
---
# <a name="discovering-device-format-capabilities"></a>Detección de capacidades de formato de dispositivo

Es posible que la aplicación intente determinar las capacidades de reproducción de un dispositivo antes de enviarle un archivo. Si un dispositivo no puede controlar el formato de un archivo que desea enviar, es posible que la aplicación intente transcodificar el archivo en un formato que pueda usar el dispositivo o notificar al usuario que el dispositivo no admite el archivo solicitado.

Tenga en cuenta que algunos dispositivos, como los dispositivos de clase de almacenamiento masivo, pueden servir únicamente como medios de almacenamiento extraíbles sin capacidad de reproducción. En este caso, sería inadecuado para la aplicación transcodificar un archivo antes de enviarlo al dispositivo.

Aunque el método [**IWMDMDevice:: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) permite a un dispositivo informar de sus capacidades, algunos dispositivos devuelven valores incorrectos para este método. Antes de copiar un archivo en un dispositivo, es posible que desee preguntar al usuario si la reproducción está pensada y, en caso afirmativo, intentar transcodificar el archivo a uno de los formatos notificados del dispositivo (o un formato razonable, si el dispositivo es compatible con cualquier formato). Otro enfoque consiste en suponer que los formatos que se enumeran específicamente como admitidos por el dispositivo están diseñados para la reproducción y que todos los demás archivos se deben transferir sin modificar.

Después de detectar el formato del archivo que se va a transferir y los formatos admitidos por un dispositivo, puede decidir cuál es el mejor formato de destino para la transcodificación.

En el pasado, era habitual que una aplicación devolvera cero para una propiedad para indicar la compatibilidad con los valores de esa propiedad. Por ejemplo, un valor de cero para [**\_ WAVEFORMATEX**](-waveformatex.md). nSamplesPerSec indicaría compatibilidad con cualquier velocidad de bits. Ahora, el método recomendado para indicar que la compatibilidad con cualquier valor es especificar \_ valores válidos de la enumeración de WMDM \_ \_ en la \_ \_ [**\_ \_ Descripción de propiedades de WMDM**](wmdm-prop-desc.md). ValidValuesForm. Sin embargo, algunas propiedades pueden devolver cero legítimamente para indicar una compatibilidad específica. Por ejemplo, si [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage se establece en cero, significa que se trata de un \_ mapa de bits RGB de BI. Las excepciones para los valores cero se indican en la documentación de las estructuras pertinentes.

Sin embargo, es importante tener en cuenta que, a menudo, los dispositivos no informan correctamente de sus capacidades de formato o de forma estándar. Por ejemplo, los dispositivos suelen informar de que admiten cualquier formato, cuando en realidad solo pueden controlar formatos específicos o velocidades de bits específicas dentro de un tipo de formato. Depende de usted decidir si su aplicación debe aceptar dichos informes o si debe asumir algún tipo de límite superior para las capacidades de reproducción de un dispositivo (por ejemplo, 192 kbps).

El método recomendado para solicitar la compatibilidad con el formato de un dispositivo es [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Si no se admite este método, la aplicación debería revertir a [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport**, a diferencia de **GetFormatSupport2**, no devuelve información de vídeo.

La forma en que una aplicación solicita las funciones de formato de un dispositivo depende de la interfaz que admita la aplicación. Para obtener más información, consulte los siguientes temas:

-   [Obtener capacidades de formato en los dispositivos que admiten IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Obtener capacidades de formato en dispositivos que solo admiten IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




