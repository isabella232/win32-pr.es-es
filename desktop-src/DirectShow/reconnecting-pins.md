---
description: Volver a conectar PIN
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Volver a conectar PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537143"
---
# <a name="reconnecting-pins"></a>Volver a conectar PIN

Durante una conexión de PIN, un filtro puede desconectar y volver a conectar uno de sus otros PIN, como se indica a continuación:

1.  El filtro llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN del otro filtro y especifica el nuevo tipo de medio.
2.  Si **QueryAccept** devuelve S \_ OK, el filtro llama a [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) para volver a conectar los pin.

A continuación se muestran algunos ejemplos de Cuándo puede ser necesario volver a conectar los pin de un filtro:

-   **Los filtros tee.** Un *filtro Tee* divide un flujo de entrada en varias salidas sin cambiar los datos en la secuencia. Un filtro Tee puede aceptar un intervalo de tipos de medios, pero los tipos deben coincidir en todas las conexiones de PIN. Por lo tanto, cuando se conecta el PIN de entrada, es posible que el filtro tenga que volver a negociar las conexiones existentes en los terminales de salida y viceversa. Para obtener un ejemplo, vea el [ejemplo de filtro InfTee](inftee-filter-sample.md).
-   **Filtros transin situ.** Un filtro *de transferencia en contexto* modifica los datos de entrada en el búfer original en lugar de copiar los datos en un búfer de salida independiente. Un filtro de transferencia en contexto debe usar el mismo asignador para las conexiones ascendentes y descendentes. El primer PIN para conectarse (entrada o salida) negocia un asignador de la manera habitual. Sin embargo, cuando se conecta el otro PIN, es posible que el primer asignador no sea aceptable. En ese caso, el segundo PIN elige un asignador diferente y el primer PIN se vuelve a conectar con el nuevo asignador. Para ver una implementación de ejemplo, vea la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .

En el método **ReconnectEx** , el administrador de gráficos de filtro desconecta y vuelve a conectar de forma asincrónica los pin. El filtro no debe intentar la reconexión a menos que **QueryAccept** devuelva los elementos \_ correctos. De lo contrario, el PIN se quedará desconectado, lo que provocará errores de gráfico. Además, el filtro debe solicitar la reconexión desde dentro del método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , en el mismo subproceso. Si el método **Connect** devuelve en un subproceso, mientras que otro subproceso realiza la solicitud de reconexión, el administrador de gráficos de filtros podría ejecutar el gráfico antes de que se vuelva a establecer la conexión, lo que provocaría errores de gráfico.

 

 



