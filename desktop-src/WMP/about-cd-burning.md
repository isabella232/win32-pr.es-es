---
title: Acerca de la grabación de CD
description: Acerca de la grabación de CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Reproductor de Windows Media,cds
- Reproductor de Windows Media de objetos, cds
- modelo de objetos, grabación de CD
- Reproductor de Windows Media ActiveX, cds
- ActiveX control, grabación de CD
- Reproductor de Windows Media Control de ActiveX móvil, grabación de CD
- Reproductor de Windows Media Móvil, grabación de CD
- Cdsar, acerca de
- cds, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c784765a09b601da2f0ec75434a37f55a75ff7e6ab6d737f7912daab8f197c07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957145"
---
# <a name="about-cd-burning"></a>Acerca de la grabación de CD

El SDK Reproductor de Windows Media 11 presenta una nueva funcionalidad para crear CD. Este proceso se denomina *insondación.*

Para enumerar las unidades de CD en el equipo del usuario, use la **interfaz IWMPCdromCollection.** Para recuperar un puntero a esta interfaz, llame a [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Mediante los **métodos count** y **item,** puede iterar la colección para recuperar un puntero de interfaz **IWMPCdrom** para cada unidad de CD en el equipo del usuario. La **interfaz IWMPCdrom** representa una unidad de CD individual.

Antes de empezar a grabar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la **interfaz IWMPCdromInterface.** Mediante el método **isAvailable,** puede determinar si una unidad de CD determinada puede grabar CD, si hay un CD en la unidad y cómo se puede usar el CD.

Para especificar los elementos que se grabarán en CD, debe crear una lista de reproducción. Reproductor de Windows Media listas de reproducción mediante la **interfaz IWMPPlaylist.** Puede crear esta lista de reproducción de la forma que quiera. Por ejemplo, puede recuperar simplemente una lista de reproducción de la biblioteca llamando a [IWMPMediaCollection::getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Después de crear la lista de reproducción que desea grabar en CD, debe llamar al método [IWMPCdromAsync::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) y pasar el puntero de lista de reproducción como argumento. Esto establece la lista de reproducción como la que Reproductor de Windows Media copiará en el CD.

Si recupera una lista de reproducción de la biblioteca, los cambios que realice en la lista de reproducción se reflejarán en la biblioteca del usuario. Para evitar esto, llame a [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo)y pase el nombre de atributo "Temporary" y el valor "true". Esto convierte la instancia de la lista de reproducción en una lista de reproducción temporal, que se puede editar sin cambiar la lista de reproducción original.

Cada vez que establezca una nueva lista de reproducción para la grabación o realice cambios en una lista de reproducción de grabación existente, debe llamar a [IWMPCdromRomRom::refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) para actualizar la información de estado. Esto garantiza que Reproductor de Windows Media el procesamiento necesario para proporcionarle información de estado precisa para la operación de grabación de CD.

Para especificar el tipo de CD que se grabará, llame [a IWMPCdromCombinación::p ut \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Reproductor de Windows Media permite grabar dos tipos de CD: cds de audio y de datos. La [enumeración WMPFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) define los tipos de CD.

Puede especificar una etiqueta de volumen para el CD mediante una llamada [a IWMPCdrom Raid::p ut \_ label](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Cuando esté listo para empezar a grabar el CD, llame a [IWMPCdromRomRom::startRom](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). Puede supervisar el progreso de la operación de grabación llamando periódicamente a [IWMPCdromRom::get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Este método recupera un valor de progreso para toda la operación de grabación. El valor recuperado es un número que representa el porcentaje de desmanes completados. Puede supervisar el estado de la operación de grabación controlando el evento [IWMPEvents3::CdromStateChange,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) que usa la enumeración [WMPState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) para indicar el estado actual. Debe tener cuidado de comparar el puntero **IWMPCdromChanged** (proporcionado por el evento ) con el puntero que representa la operación de grabación para asegurarse de que la operación ha producido el evento. Puede detener la operación de desenmascarado llamando [a IWMPCdromRomRom::stopRom](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Hay dos eventos que puede controlar para recibir notificaciones de error sobre la operación de desmantelación. El [evento IWMPEvents3::CdromError se](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) genera cuando se produce un error genérico. [IWMPEvents3::CdromRomRomMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) se genera cuando un elemento multimedia determinado produce un error durante la grabación. Al igual que el evento **CdromStateChange,** cada uno de estos eventos proporciona un puntero **IWMPCdromRom Que** representa la operación de grabación que ha producido el evento. El **evento CdromErrorMediaError** proporciona un **puntero IDispatch** que representa el elemento multimedia que ha producido el evento. Puede llamar a **QueryInterface a través** de este puntero para recuperar un **puntero IWMPMedia.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPCdrom (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**IWMPCdromRom Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**IWMPCdromCollection (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents3 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPMedia (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Atributo temporal**](temporary-attribute.md)
</dt> </dl>

 

 




