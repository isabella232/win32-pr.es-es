---
title: Monikers asincrónicos y sincrónicos
description: Monikers asincrónicos y sincrónicos
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104554490"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Monikers asincrónicos y sincrónicos

Normalmente, un cliente de un moniker OLE sincrónico estándar crea y mantiene una referencia al moniker, así como el contexto de enlace que se va a utilizar durante el enlace. Los componentes implicados en el uso de monikers tradicionales se muestran en el diagrama siguiente.

![Diagrama que muestra el cliente conectado a un contexto de enlace o a cualquier moniker para el proporcionado por el sistema.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Los clientes suelen crear monikers estándar mediante una llamada a funciones como [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)o [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) o, ya que se pueden guardar en el almacenamiento persistente, a través de [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) y [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). Los monikers también se pueden obtener de un objeto contenedor llamando al método [**IBindHost:: CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) . Los clientes crean contextos de enlace mediante una llamada a la función [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) y, a continuación, pasan el contexto de enlace al moniker con llamadas a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Como se muestra en el diagrama siguiente, un cliente de un moniker asincrónico también crea y mantiene una referencia al moniker y al contexto de enlace que se utilizarán durante el enlace.

![Diagrama que muestra las conexiones entre las proporcionadas por el cliente, las proporcionadas por el Monker y las proporcionadas por el sistema.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Para obtener el comportamiento asincrónico, el cliente implementa la interfaz [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) en un objeto de devolución de llamada de estado de enlace y llama a la función [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) o a la función [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) para registrar esta interfaz con el contexto de enlace. El moniker pasa un puntero a su interfaz [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) en una llamada al método [**IBindStatusCallback:: OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) . El cliente indica al moniker asincrónico cómo desea enlazar en la devolución de la llamada del moniker al método [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 