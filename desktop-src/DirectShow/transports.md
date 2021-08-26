---
description: Transportes
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb55542e87939168d1d95350fd71081833e4263f342a3e67c00a7c6814d51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903725"
---
# <a name="transports"></a>Transportes

Para mover datos multimedia a través del gráfico de filtros, un filtro DirectShow debe admitir uno de varios protocolos posibles. Estos protocolos se denominan transportes. Cuando se conectan dos filtros, deben admitir el mismo transporte; de lo contrario, no pueden intercambiar datos multimedia. Normalmente, un transporte requiere que uno de los pines admita una interfaz determinada. Cuando se conectan los filtros, un pin consulta al otro para la interfaz .

La DirectShow filtros de almacenamiento contiene datos multimedia en la memoria principal y los entrega a otros filtros a través de conexiones de pin. Este tipo de transporte se denomina transporte de memoria local. Aunque el transporte de memoria local es el transporte más común DirectShow, no todos los filtros lo usan. Por ejemplo, algunos filtros envían datos multimedia a lo largo de una ruta de acceso de hardware y usan pins solo para entregar información de control. Por ejemplo, vea la [**interfaz IOverlay.**](/windows/desktop/api/Strmif/nn-strmif-ioverlay)

DirectShow define dos mecanismos para el transporte de memoria local, el modelo de inserción y el modelo de extracción. En el modelo de inserción, un filtro de origen genera datos y los entrega al siguiente filtro de nivel inferior. Ese filtro recibe pasivamente los datos, los procesa y los envía más abajo. En el modelo de extracción, el filtro de origen está conectado a un filtro de analizador. El filtro del analizador solicita datos del filtro de origen. El filtro de origen responde a las solicitudes mediante la entrega de datos. El modelo de inserción usa [**la interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) y el modelo de extracción usa la [**interfaz IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

El modelo de inserción es más común que el modelo de extracción. Por lo tanto, los artículos siguientes asumen un modelo de inserción. En el último artículo de esta sección, [Pull Model (Modelo](pull-model.md)de extracción), se describe cómo la interfaz **IAsyncReader** difiere de **IMemInputPin.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



