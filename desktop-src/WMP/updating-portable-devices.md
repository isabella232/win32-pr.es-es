---
title: Actualización de dispositivos portátiles
description: Actualización de dispositivos portátiles
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Reproductor de Windows Media en línea, actualizar dispositivos portátiles
- tiendas en línea, actualizar dispositivos portátiles
- tiendas en línea de tipo 1, actualizar dispositivos portátiles
- Reproductor de Windows Media en línea, dispositivos portátiles
- tiendas en línea, dispositivos portátiles
- tiendas en línea de tipo 1, dispositivos portátiles
- actualizar dispositivos portátiles
- dispositivos portátiles, actualizar
- dispositivos portátiles, Reproductor de Windows Media en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6abc07eeecd61d287308bcc256c01f321219968d33d400b5b79aeff33d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001665"
---
# <a name="updating-portable-devices"></a>Actualización de dispositivos portátiles

Reproductor de Windows Media permite a los usuarios sincronizar contenido multimedia digital con dispositivos portátiles. Esto puede incluir contenido de música comprado o alquilado en una tienda en línea. En algunas circunstancias, es posible que los proveedores de tiendas en línea quieran escribir código para que funcione en un dispositivo portátil conectado como parte de la administración del contenido proporcionado por la tienda. Para ofrecer al complemento de la tienda en línea la oportunidad de trabajar con un dispositivo conectado, Reproductor de Windows Media llama a [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) y proporciona el nombre canónico del dispositivo portátil. Si el código del complemento determina que se debe realizar algún trabajo con el dispositivo conectado, debe devolver inmediatamente S OK de la llamada a UpdateDevice antes de continuar con \_ el trabajo.  Si no hay ningún trabajo que hacer, el complemento debe devolver un código de error.

Cuando el complemento haya terminado de usar el dispositivo, debe llamar a [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) para notificar a Reproductor de Windows Media que el dispositivo está disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




