---
title: Uso de contenido de medición
description: Uso de contenido de medición
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Uso Administrador de dispositivos multimedia, medición del uso de contenido
- Administrador de dispositivos, medición del uso de contenido
- guía de programación, medición del uso de contenido
- aplicaciones de escritorio, medición del uso de contenido
- crear Windows aplicaciones de Administrador de dispositivos multimedia, medición del uso de contenido
- uso de contenido de medición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029bae2bcdd69f9dc58c4a64317f974538c672b1d27597fbdc1915074aff0278
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957205"
---
# <a name="metering-content-usage"></a>Uso de contenido de medición

Con Windows media 10, ahora puede medir el uso de contenido en un dispositivo portátil. Si una licencia Windows Media 10 permite la medición, el dispositivo puede almacenar el recuento de reproducción de las canciones y cargar el uso de nuevo en el emisor de licencias a través de Internet. Este sistema permite a los proveedores de contenido ajustar sus cuotas de canon mediante la medición precisa del uso del contenido.

Para medir el contenido, la aplicación debe tener un certificado de medición proporcionado por un servicio de licencias basado en el SDK Windows Media Rights Manager 10. Solo se puede medir el contenido con licencia de este mismo servicio. Para obtener más información sobre cómo funciona la medición y cómo crear un servicio de medición de licencias, consulte la documentación del SDK de [Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10)) en MSDN. El SDK se puede adquirir rellenando la información necesaria en la página de licencias Windows [multimedia](https://www.microsoft.com/licensing/default).

Una aplicación puede tener la medición integrada, o bien puede compilar un complemento COM para una aplicación existente, como Reproductor de Windows Media, si la aplicación acepta complementos de medición.

Una aplicación debe advertir a los usuarios si se medirá el uso del contenido. Para obtener más información, vea las páginas web de Microsoft que aparecen en declaración [de privacidad](privacy-statement.md).

La adquisición de datos de medición desde un dispositivo puede ser lenta. Por lo tanto, si una aplicación medidora el uso, debe hacerlo con frecuencia para evitar que se acumulen grandes cantidades de datos en el dispositivo y ralentizar la transferencia de datos. Para evitar transferencias de datos que serían demasiado lentas, los fabricantes de dispositivos pueden enviar subconjuntos de datos de medición disponibles. La aplicación debe supervisar las marcas recuperadas por [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md) para ver si quedan más datos de medición en el dispositivo.

Los pasos siguientes muestran cómo una aplicación puede medir el uso de contenido.

1.  Dado que la medición solo está disponible en los dispositivos que admiten Windows Media DRM 10 para dispositivos portátiles, la aplicación debe llamar en algún momento a **QueryDeviceStatus**, como se describe en Control de contenido protegido en la aplicación [,](handling-protected-content-in-the-application.md)para asegurarse de que el dispositivo es válido y actualizado.
2.  Solicite información de medición del dispositivo mediante una [**llamada a IWMDRMDeviceApp::GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Envíe los datos de medición recuperados al servicio de medición en la dirección URL recuperada por **GenerateMeterChallenge**. El formato de los datos enviados al servicio depende del scripting de ese servicio en particular. Por ejemplo, algunos servicios pueden requerir los datos enviados como un comando POST como un par nombre-valor. El proveedor de servicios debe permitirle conocer sus requisitos de formato concretos.
4.  Obtenga una respuesta del servicio de medición y envíela al dispositivo mediante una llamada a [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md). Esto hace que el dispositivo restablezca los recuentos de reproducción y también devuelve un valor que indica si existen más datos de medición en el dispositivo que se deben recuperar llamando de nuevo a **GenerateMeterChallenge.**

Para obtener información amplia y código de ejemplo para la medición, vea el [Windows web de Media](/previous-versions//bb614723(v=vs.85)).

 

 