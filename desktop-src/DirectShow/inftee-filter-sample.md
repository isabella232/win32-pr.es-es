---
description: Ejemplo de filtro inftee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Ejemplo de filtro inftee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398023"
---
# <a name="inftee-filter-sample"></a>Ejemplo de filtro inftee

## <a name="description"></a>Descripción

El filtro InfTee proporciona una implementación de ejemplo del DirectShow [tee de pin infinito.](infinite-pin-tee-filter.md) El filtro tiene un pin de entrada y un número dinámico de pines de salida. Todos los ejemplos de medios enviados al filtro se entregan simultáneamente desde todos los pines de salida.

Este filtro aparece en GraphEdit con el nombre "Sample Infinite Pin Tee", para distinguirlo del filtro tee de pin infinito estándar que se proporciona en DirectShow.

## <a name="usage"></a>Uso

Dado que este filtro no cambia los datos que recibe, todos los pines deben aceptar el mismo tipo de medio. Durante el proceso de conexión, el filtro podría volver a conectar algunos pines para que los tipos de medios coincidan.

Los datos que llegan al pin de entrada no se copian antes de enviarse a los pins de salida. El filtro también garantiza que los datos se entregan a los filtros de nivel inferior, para garantizar que ambas salidas reciben el servicio a tiempo. En concreto, si una de las salidas puede bloquearse en la función miembro [**COutputQueue::Receive,**](coutputqueue-receive.md) la tee gira un subproceso para entregar el ejemplo. Si no hubiera ningún subproceso para entregar la muestra, el subproceso que entrega la muestra al pin de entrada de tee podría pasar los datos a un filtro de bajada; en ese momento, podría bloquearse, manteniendo los datos del otro filtro de bajada durante largos períodos de tiempo.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente de [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ InfTee.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



