---
title: Cómo funcionan el enlace asincrónico Storage trabajo
description: El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga de objetos de almacenamiento en redes de alta latencia y vínculos lentos, como Internet.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Cómo funcionan el enlace asincrónico Storage trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176ff85044210a94cecf2649fa7475eae2b291def43b0876d2ecbc9c98b0866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961905"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Cómo funcionan el enlace asincrónico Storage trabajo

El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga de objetos de almacenamiento en redes de alta latencia y vínculos lentos, como Internet. El almacenamiento asincrónico funciona junto con monikers asincrónicos para proporcionar un comportamiento de enlace asincrónico completo.

## <a name="document-object-embedded-in-a-web-page"></a>Objeto de documento insertado en una página web

Cuando un usuario hace clic en un vínculo que representa un documento incrustado en una página web, se producen los siguientes eventos:

1.  El explorador llama a la [**función MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) y pasa la dirección URL del vínculo.
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analiza la dirección URL, crea un moniker asincrónico correspondiente y devuelve un puntero a la interfaz [**IMoniker del moniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)
3.  El explorador llama a [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) para determinar si el moniker es asincrónico, crea un contexto de enlace, registra la interfaz [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con el contexto de enlace, solo si el moniker es asincrónico y llama a [**IMoniker::BindToObject,**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)pasando el contexto de enlace.
4.  El moniker se enlaza al objeto y lo consulta para la interfaz [**IPersistMoniker,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) que indica si el objeto admite el enlace asincrónico y el almacenamiento. Si el objeto devuelve un puntero a **IPersistMoniker**:

    1.  El moniker de dirección URL llama a [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))y pasa su propio [**puntero IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) al objeto .
    2.  El objeto modifica el contexto de enlace, elige si desea un almacenamiento de bloqueo o no, registra su propio [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) y llama a [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) en el puntero que recibió a través de [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  El moniker crea un almacenamiento asincrónico, mantiene una referencia a la interfaz [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) del objeto contenedor, registra la interfaz [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) en el almacenamiento raíz y llama a [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), pasando el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del almacenamiento asincrónico. A medida que llegan los datos (en un subproceso en segundo plano), el moniker llama a **IFillLockBytes** para rellenar [**los ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) en el archivo temporal.
    4.  El objeto lee datos del almacenamiento y devuelve de [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) cuando ha recibido datos suficientes para considerarse inicializado. Si el objeto intenta leer datos que aún no se han descargado, el descargador recibe una notificación en [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro del método [**IProgressNotify::OnProgress,**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) el subproceso de descarga se bloquea en un bucle de mensajes modal o hace que el almacenamiento asincrónico devuelva E PENDING, en función de si el objeto ha solicitado un almacenamiento de bloqueo o de no \_ bloqueo.

5.  Si el objeto no implementa [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), el moniker consulta [**para IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), lo que indica que el estado persistente del objeto se almacena en un objeto de almacenamiento. Si el objeto devuelve un puntero a **IPersistStorage**:

    1.  El Moniker llama a [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) en sí mismo, solicitando un [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de bloqueo (porque el objeto no es asincrónico), crea un almacenamiento asincrónico, mantiene una referencia a la interfaz [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) del objeto contenedor, registra la interfaz [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) en el almacenamiento raíz y llama a [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), pasando el puntero **IStorage** del almacenamiento asincrónico. A medida que llegan los datos (en un subproceso en segundo plano), el moniker llama a [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) para rellenar [**los ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) en el archivo temporal.
    2.  El objeto lee datos del almacenamiento y devuelve de [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) cuando ha recibido datos suficientes para considerarse inicializado. Si el objeto intenta leer datos que aún no se han descargado, recibe una notificación en [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro del [**método IProgressNotify::OnProgress,**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) el subproceso de descarga siempre se bloquea en un bucle de mensajes modal.

6.  Independientemente de si la descarga es sincrónica o asincrónica, el moniker devuelve de [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)y el explorador recibe el objeto inicializado que solicitó.
7.  El explorador consulta [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) y hospeda el objeto como un objeto document. (En este momento, es posible que el objeto no se inicialice completamente, pero suficiente para mostrar algo útil, en cuyo caso la descarga continúa en segundo plano).

 

 