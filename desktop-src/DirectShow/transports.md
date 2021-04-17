---
description: Transportes
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687726"
---
# <a name="transports"></a>Transportes

Para poder trasladar los datos multimedia a través del gráfico de filtro, un filtro DirectShow debe admitir uno de varios protocolos posibles. Estos protocolos se denominan transportes. Cuando dos filtros se conectan, deben admitir el mismo transporte. en caso contrario, no pueden intercambiar datos multimedia. Normalmente, un transporte requiere que uno de los pin admita una interfaz determinada. Cuando los filtros se conectan, un PIN consulta el otro para la interfaz.

La mayoría de los filtros de DirectShow contienen datos multimedia en la memoria principal y los entregan a otros filtros a través de conexiones de PIN. Este tipo de transporte se denomina transporte de memoria local. Aunque el transporte de memoria local es el transporte más común en DirectShow, no todos los filtros lo usan. Por ejemplo, algunos filtros envían datos multimedia a lo largo de una ruta de hardware y usan PIN solo para proporcionar información de control. Por ejemplo, vea la interfaz [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .

DirectShow define dos mecanismos para el transporte de memoria local, el modelo de inserción y el modelo de extracción. En el modelo de insertar, un filtro de origen genera datos y los entrega al siguiente filtro de nivel inferior. Ese filtro recibe los datos de forma pasiva, los procesa y los envía más abajo. En el modelo de extracción, el filtro de origen se conecta a un filtro de analizador. El filtro del analizador solicita datos del filtro de origen. El filtro de origen responde a las solicitudes mediante la entrega de datos. El modelo de inserción usa la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) y el modelo de extracción usa la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

El modelo de inserción es más común que el modelo de extracción. Por lo tanto, los artículos siguientes suponen un modelo de inserciones. El último artículo de esta sección, [modelo de extracción](pull-model.md), describe el modo en que la interfaz **IAsyncReader** difiere de **IMemInputPin**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



