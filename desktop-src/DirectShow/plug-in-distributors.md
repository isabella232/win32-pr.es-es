---
description: Distribuidores de complementos
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Distribuidores de complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686328"
---
# <a name="plug-in-distributors"></a>Distribuidores de complementos

Los distribuidores de complementos (PID) son una forma de ampliar la funcionalidad del administrador de gráficos de filtro. Un distribuidor de complementos es un objeto COM que el administrador de gráficos de filtro agrega en tiempo de ejecución. Las aplicaciones obtienen acceso al PID a través del administrador de gráficos de filtro.

Cuando se consulta el administrador de gráficos de filtro para una interfaz que no admite, busca una clave en el registro con el siguiente formato:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` es una cadena que contiene el identificador de interfaz. Si existe la entrada del registro, el valor de la entrada define el identificador de clase (CLSID) de un PID que admite la interfaz. El administrador de gráficos de filtros agrega el PID y devuelve un puntero de interfaz, con lo que actúa como **IUnknown** exterior para el PID. Cuando la aplicación llama a métodos en la interfaz, realmente los llama en el PID. Sin embargo, la existencia del PID es transparente para la aplicación.

El término *distribuidor* se deriva del hecho de que un PID puede consultar su puntero **IUnknown** externo para las interfaces en el administrador de gráficos de filtro. Al llamar al método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , el PID puede enumerar los filtros del gráfico y distribuir las llamadas de método a esos filtros. De esta manera, un PID puede actuar como un único punto de control para que la aplicación llame a métodos en filtros.

Cuando el administrador de gráficos de filtro agrega un PID, consulta el PID de la interfaz [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) . Si el PID es compatible con esta interfaz, el administrador de gráficos de filtros la usa para notificar a los PID los cambios en el gráfico:

-   Cuando el gráfico de filtro cambia entre los Estados de ejecución, pausa y detenida, llama a [**IDistributorNotify:: Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)o [**IDistributorNotify:: Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Cuando se establece un reloj de referencia, el administrador de gráficos de filtros llama a [**IDistributorNotify:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Cuando se agregan o quitan filtros o se cambian las conexiones de PIN, el administrador de gráficos de filtros llama a [**IDistributorNotify:: NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Para implementar un PID personalizado, cree un objeto COM que admita la agregación. Debe ser compatible con una interfaz que no admita el administrador de gráficos de filtro. Opcionalmente, puede admitir la interfaz **IDistributorNotify** .

Si el PID obtiene todos los punteros de interfaz del administrador de gráficos de filtro, debe liberarlos inmediatamente. De lo contrario, podría crear un recuento de referencias circulares, lo que podría impedir que se destruyese el administrador de gráficos de filtro. No es necesario mantener un recuento de referencias en el administrador de gráficos de filtro en ningún caso, ya que el administrador de gráficos de filtro controla la duración del PID.

Dado que un PID está diseñado específicamente para la agregación mediante el administrador de gráficos de filtro, es posible que desee aplicar esto en el método de constructor del PID. Compruebe si el puntero **IUnknown** externo es **null** y, en caso afirmativo, devuelva el código de error VFW \_ E \_ necesito \_ Owner. (Consulte los [códigos de error y de éxito](error-and-success-codes.md)). Además, para evitar que otros objetos agreguen el PID, puede consultar el puntero **IUnknown** externo de la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Devuelve un código de error si el objeto no expone **IGraphBuilder**.

 

 



