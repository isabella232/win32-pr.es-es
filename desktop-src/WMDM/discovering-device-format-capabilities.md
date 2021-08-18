---
title: Detección de funcionalidades de formato de dispositivo
description: Detección de funcionalidades de formato de dispositivo
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Características de Administrador de dispositivos multimedia, funcionalidades del dispositivo
- Administrador de dispositivos, funcionalidades del dispositivo
- guía de programación, funcionalidades del dispositivo
- aplicaciones de escritorio, funcionalidades de dispositivo
- creación de Windows aplicaciones Administrador de dispositivos multimedia, funcionalidades del dispositivo
- escribir archivos en dispositivos, funcionalidades del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4fc32c0980a1022f7affb225918ccf0d49e5d14c5bb7310e70e7aa4f83a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585151"
---
# <a name="discovering-device-format-capabilities"></a>Detección de funcionalidades de formato de dispositivo

Es posible que la aplicación intente determinar las funcionalidades de reproducción de un dispositivo antes de enviarle un archivo. Si un dispositivo no puede controlar el formato de un archivo que desea enviar, la aplicación podría intentar transcodificar el archivo en un formato que el dispositivo pueda usar o notificar al usuario que el dispositivo no puede admitir el archivo solicitado.

Tenga en cuenta que algunos dispositivos, como los dispositivos de clase de almacenamiento masivo, solo pueden servir como medios de almacenamiento extraíbles sin funcionalidades de reproducción. En este caso, sería inadecuado que la aplicación transcodifique un archivo antes de enviarlo al dispositivo.

Aunque el [**método IWMDMDevice::GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) permite que un dispositivo informe de sus funcionalidades, algunos dispositivos devuelven valores incorrectos para este método. Antes de copiar un archivo en un dispositivo, es posible que quiera preguntar al usuario si la reproducción está prevista y, si es así, intentar transcodificar el archivo en uno de los formatos notificados del dispositivo (o un formato razonable, si el dispositivo solicita compatibilidad con cualquier formato). Otro enfoque es asumir que los formatos enumerados específicamente como compatibles con el dispositivo están diseñados para la reproducción y que todos los demás archivos deben transferirse sin modificar.

Después de detectar el formato del archivo que se va a transferir y los formatos admitidos por un dispositivo, puede decidir cuál es el mejor formato de destino para la transcodificación.

En el pasado, era habitual que una aplicación devolvía cero para una propiedad para indicar la compatibilidad con los valores de esa propiedad. Por ejemplo, un valor de cero para [**\_ DESATEX**](-waveformatex.md).nSamplesPerSec indicaría la compatibilidad con cualquier velocidad de bits. Ahora, la manera recomendada de indicar la compatibilidad con cualquier valor es especificar WMDM \_ ENUM \_ PROP VALID VALUES ANY en \_ \_ \_ [**WMDM PROP \_ \_ DESC**](wmdm-prop-desc.md). ValidValuesForm. Sin embargo, algunas propiedades pueden devolver legítimamente cero para indicar compatibilidad específica. Por ejemplo, si [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md).biSizeImage está establecido en cero, esto indica un mapa de \_ bits RGB de BI. Las excepciones para los valores cero se anotan en la documentación de las estructuras pertinentes.

Sin embargo, es importante tener en cuenta que los dispositivos a menudo no informan de sus funcionalidades de formato correctamente o de forma estándar. Por ejemplo, los dispositivos a menudo informan de que admiten cualquier formato, cuando de hecho solo pueden controlar formatos específicos o velocidades de bits específicas dentro de un tipo de formato. Es decisión del usuario decidir si la aplicación debe aceptar estos informes o si debe asumir algún tipo de límite superior a las capacidades de reproducción de un dispositivo (por ejemplo, 192 kbps).

El método recomendado para solicitar la compatibilidad de formato de un dispositivo [**es IWMDMDevice3::GetFormatCapability.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) Si no se admite este método, la aplicación debe volver a [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport,** a **diferencia de GetFormatSupport2,** no devuelve información de vídeo.

La forma en que una aplicación solicita las funcionalidades de formato de un dispositivo depende de la interfaz que admita la aplicación. Para obtener más información, consulte los siguientes temas:

-   [Obtención de funcionalidades de formato en dispositivos que admiten IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Obtención de funcionalidades de formato en dispositivos que solo admiten IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




