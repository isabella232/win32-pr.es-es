---
title: Uso del contenido de disponibilidad
description: Uso del contenido de disponibilidad
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Media Administrador de dispositivos, uso de contenido de medición
- Administrador de dispositivos, uso del contenido de medición
- Guía de programación, uso de contenido de medición
- aplicaciones de escritorio, uso de contenido de medición
- crear aplicaciones de Windows Media Administrador de dispositivos, uso de contenido de medición
- uso del contenido de disponibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105695795"
---
# <a name="metering-content-usage"></a>Uso del contenido de disponibilidad

Con la tecnología de Windows Media 10, ahora puede medir el uso de contenido en un dispositivo portátil. Si una licencia de Windows Media 10 permite la medición, el dispositivo puede almacenar el número de repeticiones de canciones y volver a cargar el uso en el emisor de la licencia a través de Internet. Este sistema permite a los proveedores de contenido ajustar sus tarifas de regalías mediante la medición exacta del uso del contenido.

Para medir el contenido, la aplicación debe tener un certificado de medición proporcionado por un servicio de licencias basado en el SDK de Windows Media Rights Manager 10. Solo se puede medir el contenido con licencia de este mismo servicio. Para obtener más información sobre cómo funciona la medición y cómo crear un servicio de medición de licencias, consulte la [documentación del SDK de Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10)) en MSDN. El SDK se puede adquirir rellenando la información necesaria en la [Página de licencias de Windows Media](https://www.microsoft.com/licensing/default).

Una aplicación puede tener una medida integrada, o bien puede crear un complemento COM para una aplicación existente, como el Media Player de Windows, si la aplicación acepta complementos de medición.

Una aplicación debe advertir a los usuarios si se medirá el uso del contenido. Para obtener más información, vea las páginas web de Microsoft enumeradas en la [declaración de privacidad](privacy-statement.md).

La adquisición de datos de medición desde un dispositivo puede ser lenta. Por lo tanto, si una aplicación mide el uso, debe hacerlo con frecuencia para evitar que una gran cantidad de datos se acumule en el dispositivo y ralentice la transferencia de datos. Para evitar que las transferencias de datos sean demasiado lentas, los fabricantes de dispositivos pueden enviar subconjuntos de datos de disponibilidad disponibles. La aplicación debe supervisar las marcas recuperadas por [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) para ver si hay más datos de medición que permanecen en el dispositivo.

En los pasos siguientes se muestra cómo una aplicación puede medir el uso de contenido.

1.  Dado que la medición solo está disponible en los dispositivos que admiten Windows Media DRM 10 para dispositivos portátiles, la aplicación debe llamar a **QueryDeviceStatus**, como se describe en [control de contenido protegido en la aplicación](handling-protected-content-in-the-application.md), para asegurarse de que el dispositivo es válido y está actualizado.
2.  Solicite información de disponibilidad del dispositivo mediante una llamada a [**IWMDRMDeviceApp:: GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Envíe los datos de medición recuperados al servicio de medición en la dirección URL recuperada por **GenerateMeterChallenge**. El formato de los datos enviados al servicio depende del scripting de ese servicio concreto. Por ejemplo, algunos servicios pueden requerir que los datos se envíen como un comando POST como un par nombre-valor. El proveedor de servicios debe permitirle conocer sus requisitos de formato concretos.
4.  Obtenga una respuesta del servicio de medición y envíelo al dispositivo llamando a [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md). Esto hace que el dispositivo restablezca los recuentos de reproducción y también devuelve un valor que indica si hay más datos de disponibilidad en el dispositivo que se deben recuperar llamando a **GenerateMeterChallenge** de nuevo.

Para obtener información y código de ejemplo para la medición, vea el [sitio web de Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 