---
title: Atributo SyncState
description: El atributo SyncState es una representación de cadena de un valor de 32 bits que Reproductor de Windows Media cuando sincroniza listas de reproducción con dispositivos portátiles.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Atributo SyncState Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7712a6e3bb0a01f4a713af114f91ebdcb302ef172c77e1cb64b8746f9ae0dcf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414865"
---
# <a name="syncstate-attribute"></a>Atributo SyncState

El **atributo SyncState** es una representación de cadena de un valor de 32 bits que Reproductor de Windows Media cuando sincroniza listas de reproducción con dispositivos portátiles.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotos](photo-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo consta de 16 valores de 2 bits, cada uno de los cuales especifica el estado de sincronización de un dispositivo portátil. El bit más significativo (MSB) de este valor de 32 bits corresponde al dispositivo 16. El bit menos significativo (LSB) corresponde al dispositivo 1.

El MSB de cada valor de 2 bits indica si Reproductor de Windows Media sincronizado el contenido con el dispositivo correspondiente. Un valor de 1 indica que lo hizo. Un valor de 0 indica que no lo hizo.

Si el MSB es 0, el LSB especifica por qué no se pudo sincronizar. Un valor de 1 en el LSB indica que no había suficiente espacio libre para el contenido. Un valor de 0 en el LSB indica algún otro motivo que impide la sincronización.

Para recuperar el estado de sincronización de un dispositivo determinado, debe hacer lo siguiente:

1.  **Invoque el estado IWMPSyncDevice::get \_** para determinar si un dispositivo determinado está sincronizado.
2.  Si está sincronizado, invoque **IWMPSyncDevice::get \_ partnershipIndex** para recuperar el índice del par de bits del dispositivo en el **atributo SyncState.**
3.  Con este índice, enmascara el par de bits correspondiente del atributo **SyncState** y examina el resultado para determinar el estado de sincronización de la lista de reproducción con el dispositivo.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Determinar el estado de sincronización de la lista de reproducción**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice::get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice::get \_ status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





