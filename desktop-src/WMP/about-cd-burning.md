---
title: Acerca de la grabación de CD
description: Acerca de la grabación de CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, acerca de
- grabar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789189"
---
# <a name="about-cd-burning"></a>Acerca de la grabación de CD

El SDK de Windows Media Player 11 presenta una nueva funcionalidad para crear CDs. Este proceso se denomina *grabación*.

Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** . Para recuperar un puntero a esta interfaz, llame a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Mediante el uso de los métodos **Count** y **Item** , puede recorrer en iteración la colección para recuperar un puntero de la interfaz **IWMPCDROM** para cada unidad de CD del equipo del usuario. La interfaz **IWMPCdrom** representa una unidad de CD individual.

Antes de empezar a grabar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la interfaz **IWMPCdromBurn** . Mediante el método **isavailable** , puede determinar si una unidad de CD determinada puede grabar CDs, si hay un CD en la unidad y cómo se puede usar el CD.

Para especificar los elementos que se van a grabar en el CD, debe crear una lista de reproducción. Windows Media Player representa listas de reproducción mediante la interfaz **IWMPPlaylist** . Puede crear esta lista de reproducción de la forma que desee. Por ejemplo, podría simplemente recuperar una lista de reproducción de la biblioteca llamando a [IWMPMediaCollection:: getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Después de crear la lista de reproducción que desea grabar en el CD, debe llamar al método [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) y pasar el puntero de la lista de reproducción como argumento. Esto establece la lista de reproducción como la que Windows Media Player copiará en el CD.

Si recupera una lista de reproducción de la biblioteca, los cambios que realice en la lista de reproducción se reflejarán en la biblioteca del usuario. Para evitar esto, llame a [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), pasando el nombre de atributo "Temporary" y el valor "true". Esto convierte la instancia de la lista de reproducción en una lista de reproducción temporal, que se puede editar sin cambiar la lista de reproducción original.

Cada vez que se establece una nueva lista de reproducción para grabar o se realizan cambios en una lista de reproducción de grabación existente, se debe llamar a [IWMPCdromBurn:: refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) para actualizar la información de estado. Esto garantiza que Windows Media Player realice el procesamiento necesario para proporcionar información de estado precisa para la operación de grabación de CD.

Para especificar el tipo de CD que se va a grabar, llame a [IWMPCdromBurn::p UT \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Windows Media Player permite grabar dos tipos de CDs: CDs de audio y CDs de datos. La enumeración [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) define los tipos de CD.

Puede especificar una etiqueta de volumen para el CD llamando a [IWMPCdromBurn::p \_ etiqueta UT](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Cuando esté listo para empezar a grabar el CD, llame a [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). Puede supervisar el progreso de la operación de grabación llamando periódicamente a [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Este método recupera un valor de progreso para toda la operación de grabación. El valor recuperado es un número que representa el porcentaje de la Grabación completada. Puede supervisar el estado de la operación de grabación controlando el evento [IWMPEvents3:: CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) , que usa la enumeración [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) para indicar el estado actual. Debe tener cuidado de comparar el puntero **IWMPCdromBurn** (proporcionado por el evento) con el puntero que representa la operación de grabación para asegurarse de que la operación ha generado el evento. Puede detener la operación de grabación llamando a [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Hay dos eventos que se pueden controlar para recibir notificaciones de error sobre la operación de grabación. El evento [IWMPEvents3:: CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) se genera cuando se produce un error genérico. [IWMPEvents3:: CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) se genera cuando un elemento multimedia determinado provoca un error durante la grabación. Al igual que el evento **CdromBurnStateChange** , cada uno de estos eventos proporciona un puntero **IWMPCdromBurn** que representa la operación de grabación que provocó el evento. El evento **CdromBurnMediaError** proporciona un puntero **IDispatch** que representa el elemento multimedia que provocó el evento. Puede llamar a **QueryInterface** a través de este puntero para recuperar un puntero **IWMPMedia** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interfaz IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interfaz IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**Interfaz IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interfaz IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interfaz IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interfaz IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Atributo temporal**](temporary-attribute.md)
</dt> </dl>

 

 




