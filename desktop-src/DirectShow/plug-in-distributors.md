---
description: Distribuidores de complementos
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Distribuidores de complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70d253066fdde4f082a964c56a221331cfd127c0984db2a7b1933a0bb352425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583665"
---
# <a name="plug-in-distributors"></a>Distribuidores de complementos

Los distribuidores de complementos (PID) son una manera de ampliar la funcionalidad del administrador de gráficos de filtros. Un distribuidor de complementos es un objeto COM que el administrador de gráficos de filtros agrega en tiempo de ejecución. Las aplicaciones obtienen acceso al PID a través del administrador de gráficos de filtro.

Cuando se consulta al administrador de gráficos de filtros una interfaz que no admite, busca en el Registro una clave con el formato siguiente:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` es una cadena que contiene el identificador de interfaz. Si la entrada del Registro existe, el valor de la entrada define el identificador de clase (CLSID) de un PID que admite la interfaz . El administrador de gráficos de filtro agrega el PID y devuelve un puntero de interfaz, actuando como **IUnknown** externo para el PID. Cuando la aplicación llama a métodos en la interfaz, en realidad los llama en el PID. Sin embargo, la existencia del PID es transparente para la aplicación.

El término *distribuidor* se deriva del hecho de que un PID puede consultar su puntero **IUnknown** externo para las interfaces en el administrador de gráficos de filtros. Al llamar al [**método IFilterGraph::EnumFilters,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) el PID puede enumerar los filtros del gráfico y distribuir llamadas de método a esos filtros. De esta manera, un PID puede actuar como un único punto de control para que la aplicación llame a métodos en filtros.

Cuando el administrador de gráficos de filtro agrega un PID, consulta el PID para la [**interfaz IDistributorNotify.**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) Si el PID admite esta interfaz, el administrador de gráficos de filtro lo usa para notificar al PID los cambios en el gráfico:

-   Cuando el gráfico de filtro cambia entre los estados de ejecución, pausado y detenido, llama a [**IDistributorNotify::Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)o [**IDistributorNotify::Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Cuando se establece un reloj de referencia, el administrador de gráficos de filtro llama a [**IDistributorNotify::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Cuando se agregan o quitan filtros, o se cambian las conexiones de pin, el administrador de gráficos de filtros llama a [**IDistributorNotify::NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Para implementar un PID personalizado, cree un objeto COM que admita agregaciones. Debe admitir una interfaz que el administrador de gráficos de filtros aún no admita. Opcionalmente, puede admitir la **interfaz IDistributorNotify.**

Si el PID obtiene punteros de interfaz del administrador de gráficos de filtro, debe liberarlos inmediatamente. De lo contrario, podría crear un recuento circular de referencias, lo que podría impedir que se destruyese el administrador de gráficos de filtros. Mantener un recuento de referencias en el administrador de gráficos de filtros no es necesario en ningún caso, porque el administrador de gráficos de filtro controla la duración del PID.

Dado que un PID está diseñado específicamente para su agregación por el administrador de gráficos de filtros, es posible que desee aplicarlo en el método de constructor del PID. Compruebe si el puntero **IUnknown** externo es **NULL** y, si es así, devuelva el código de error VFW \_ E NEED \_ \_ OWNER. (Vea [Códigos de error y de éxito).](error-and-success-codes.md) Además, para evitar que otros objetos agreguen el PID, puede consultar el puntero **IUnknown** externo para la [**interfaz IGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) Devuelve un código de error si el objeto no expone **IGraphBuilder.**

 

 



