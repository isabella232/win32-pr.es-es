---
description: Creación de una captura de audio Graph vista previa
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Creación de una captura de audio Graph vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5522f04e40704d635d7d4cc925fd81045579c01ae05dbdebd725611139fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108254"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>Creación de una captura de audio Graph vista previa

El gráfico de filtros descrito en Creación de una captura [de audio Graph](creating-an-audio-capture-graph.md) solo realiza la captura, sin vista previa. Para obtener una vista previa y capturar al mismo tiempo, el gráfico de filtros debe usar el filtro [tee de pin infinito](infinite-pin-tee-filter.md). Este filtro tiene un pin de entrada y crea tantos pines de salida como sea necesario. (Comienza con un pin de salida. Cada vez que se conecta un pin de salida, se crea otro). El filtro Infinite Pin Tee entrega todas las muestras que recibe, sin cambios, a través de todos sus pines de salida.

Conectar el filtro de captura de audio a la te de pin infinito y conecte la tee de pin infinito al multiplexor y al filtro de [representador de Direct Sound.](directsound-renderer-filter.md) Conectar multiplexor al escritor de archivos, como antes. En el diagrama siguiente se muestra el gráfico de filtros resultante para un archivo AVI.

![gráfico de captura de audio con versión preliminar](images/audio-capture-graph.png)

Dado que el representador de Direct Sound es el representador de audio predeterminado, simplemente puede llamar al método [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) en el pin de salida de infinite pin tee. El Administrador Graph filtros usa [Intelligent Conectar](intelligent-connect.md) para crear el representador, agregarlo al gráfico de filtros y conectar los pines.

> [!Note]  
> Si captura audio de un micrófono y la vista previa de él desde un altavoz en el mismo equipo, puede crear comentarios de audio.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



