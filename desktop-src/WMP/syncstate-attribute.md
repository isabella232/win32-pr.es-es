---
title: Atributo SyncState
description: El atributo SyncState es una representación de cadena de un valor de 32 bits que usa Windows Media Player cuando sincroniza listas de reproducción con dispositivos portátiles.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState Media Player de Windows
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718680"
---
# <a name="syncstate-attribute"></a>Atributo SyncState

El atributo **SyncState** es una representación de cadena de un valor de 32 bits que usa Windows Media Player cuando sincroniza listas de reproducción con dispositivos portátiles.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotografía](photo-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo consta de valores de 16 2 bits, cada uno de los cuales especifica el estado de sincronización de un dispositivo portátil. El bit más significativo (MSB) de este valor de 32 bits corresponde al dispositivo 16. El bit menos significativo (LSB) corresponde al dispositivo 1.

El MSB de cada valor de 2 bits indica si Windows Media Player sincronizar el contenido con el dispositivo correspondiente. Un valor de 1 indica que lo hizo. Un valor de 0 indica que no lo hizo.

Si el MSB es 0, LSB especifica por qué se produjo un error en la sincronización. Un valor de 1 en LSB indica que no hay suficiente espacio libre para el contenido. Un valor de 0 en LSB indica algún otro motivo que impidió la sincronización.

Para recuperar el estado de sincronización de un dispositivo determinado, debe hacer lo siguiente:

1.  Invocar **IWMPSyncDevice:: get \_ status** para determinar si un dispositivo determinado está sincronizado.
2.  Si está sincronizado, invoque **IWMPSyncDevice:: get \_ partnershipIndex** para recuperar el índice del par de bits del dispositivo en el atributo **SyncState** .
3.  Con este índice, debe enmascarar el par de bits correspondiente del atributo **SyncState** y examinar el resultado para determinar el estado de sincronización de la lista de reproducción con el dispositivo.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Determinar el estado de sincronización de la lista de reproducción**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice:: get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice:: get \_ status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





