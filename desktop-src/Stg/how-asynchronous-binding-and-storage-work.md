---
title: Cómo funciona el enlace asincrónico y el almacenamiento
description: El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga de objetos de almacenamiento en redes de alta latencia y vínculo de baja velocidad, como Internet.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Cómo funciona el enlace asincrónico y el almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420884"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Cómo funciona el enlace asincrónico y el almacenamiento

El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga de objetos de almacenamiento en redes de alta latencia y vínculo de baja velocidad, como Internet. El almacenamiento asincrónico funciona junto con monikers asincrónicos para proporcionar un comportamiento de enlace asincrónico completo.

## <a name="document-object-embedded-in-a-web-page"></a>Objeto de documento incrustado en una página web

Cuando un usuario hace clic en un vínculo que representa un documento incrustado en una página web, se producen los siguientes eventos:

1.  El explorador llama a la función [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) , pasando la dirección URL del vínculo.
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analiza la dirección URL, crea un moniker asincrónico correspondiente y devuelve un puntero a la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) del moniker.
3.  El explorador llama a [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) para determinar si el moniker es asincrónico, crea un contexto de enlace, registra la interfaz [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con el contexto de enlace, solo si el moniker es asincrónico y llama a [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), pasando el contexto de enlace.
4.  El moniker se enlaza al objeto y lo consulta para la interfaz [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , que indica si el objeto admite el enlace y el almacenamiento asincrónicos. Si el objeto devuelve un puntero a **IPersistMoniker**:

    1.  El moniker de dirección URL llama a [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)), pasando su propio puntero [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) al objeto.
    2.  El objeto modifica el contexto de enlace, elige si desea un almacenamiento de bloqueo o sin bloqueos, registra su propio [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) y llama a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) en el puntero que recibe a través de [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  El moniker crea un almacenamiento asincrónico, mantiene una referencia a la interfaz [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) del objeto contenedor, registra la interfaz [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) en el almacenamiento raíz y llama a [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), pasando el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del almacenamiento asincrónico. A medida que llegan los datos (en un subproceso en segundo plano), el moniker llama a **IFillLockBytes** para rellenar [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) en el archivo temporal.
    4.  El objeto Lee los datos del almacenamiento y vuelve de [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) cuando ha recibido suficientes datos que se deben inicializar. Si el objeto intenta leer los datos que aún no se han descargado, el descargador recibe una notificación en [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro del método [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , el subproceso de descarga se bloquea en un bucle de mensajes modal o hace que el almacenamiento asincrónico devuelva E \_ pendiente, dependiendo de si el objeto ha solicitado un almacenamiento de bloqueo o de no bloqueo.

5.  Si el objeto no implementa [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), el moniker consulta [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), lo que indica que el estado persistente del objeto se almacena en un objeto de almacenamiento. Si el objeto devuelve un puntero a **IPersistStorage**:

    1.  El moniker llama a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) en sí mismo, solicitando un [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de bloqueo (porque el objeto no es asincrónico), crea un almacenamiento asincrónico, mantiene una referencia a la interfaz [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) del objeto contenedor, registra la interfaz [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) en el almacenamiento raíz y llama a [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), pasando el puntero **IStorage** del almacenamiento asincrónico. A medida que llegan los datos (en un subproceso en segundo plano), el moniker llama a [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) para rellenar [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) en el archivo temporal.
    2.  El objeto Lee los datos del almacenamiento y devuelve de [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) cuando ha recibido suficientes datos que se deben inicializar. Si el objeto intenta leer los datos que aún no se han descargado, recibe una notificación en [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro del método [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , el subproceso que se descarga siempre se bloquea en un bucle de mensajes modal.

6.  Independientemente de si la descarga es sincrónica o asincrónica, el moniker devuelve de [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)y el explorador recibe el objeto inicializado que solicitó.
7.  El explorador consulta el objeto [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) y lo hospeda como un objeto de documento. (En este punto, es posible que el objeto no se inicialice por completo, pero lo suficiente para mostrar algo útil, en cuyo caso la descarga continúa en segundo plano).

 

 