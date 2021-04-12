---
title: Actualización de dispositivos portátiles
description: Actualización de dispositivos portátiles
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player tiendas en línea, actualizar dispositivos portátiles
- tiendas en línea, actualizar dispositivos portátiles
- tipo 1 almacenes en línea, actualizar dispositivos portátiles
- Windows Media Player tiendas en línea, dispositivos portátiles
- tiendas en línea, dispositivos portátiles
- tipo 1 tiendas en línea, dispositivos portátiles
- actualización de dispositivos portátiles
- dispositivos portátiles, actualizar
- dispositivos portátiles, tiendas Windows Media Player en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358670"
---
# <a name="updating-portable-devices"></a>Actualización de dispositivos portátiles

Windows Media Player permite a los usuarios sincronizar contenido multimedia digital con dispositivos portátiles. Esto puede incluir el contenido de música adquirido o alquilado desde una tienda en línea. En algunas circunstancias, los proveedores de tiendas en línea pueden querer escribir código para trabajar en un dispositivo portátil conectado como parte de la administración del contenido proporcionado por el almacén. Para que el complemento de la tienda en línea tenga la oportunidad de trabajar con un dispositivo conectado, Windows Media Player llama a [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) y proporciona el nombre canónico del dispositivo portátil. Si el código del complemento determina que se debe realizar algún trabajo con el dispositivo conectado, debe devolver de inmediato los elementos \_ correctos de la llamada a **UpdateDevice** antes de continuar con el trabajo. Si no hay ningún trabajo que hacer, el complemento debe devolver un código de error.

Cuando el complemento ha terminado de usar el dispositivo, debe llamar a [IWMPContentPartnerCallback:: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) para notificar a Windows Media Player que el dispositivo está disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




