---
description: Volver a conectar los pines
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Volver a conectar los pines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886617"
---
# <a name="reconnecting-pins"></a>Volver a conectar los pines

Durante una conexión de pin, un filtro puede desconectarse y volver a conectar uno de sus otros pines, como se muestra a continuación:

1.  El filtro llama [**a IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el pin del otro filtro y especifica el nuevo tipo de medio.
2.  Si **QueryAccept devuelve** S \_ OK, el filtro llama a [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) para volver a conectar los pines.

A continuación se muestran algunos ejemplos de cuándo es posible que un filtro necesite volver a conectar los pines:

-   **Filtros de tee.** Un *filtro de tee* divide un flujo de entrada en varias salidas sin cambiar los datos de la secuencia. Un filtro de tee puede aceptar un intervalo de tipos de medios, pero los tipos deben coincidir en todas las conexiones de pin. Por lo tanto, cuando se conecta el pin de entrada, es posible que el filtro tenga que renegociar las conexiones existentes en los pines de salida y viceversa. Para obtener un ejemplo, vea el [ejemplo de filtro InfTee](inftee-filter-sample.md).
-   **Filtros trans-in-place.** Un *filtro trans-in-place* modifica los datos de entrada en el búfer original en lugar de copiar los datos en un búfer de salida independiente. Un filtro trans-in-place debe usar el mismo asignador para las conexiones ascendentes y descendentes. El primer pin para conectarse (entrada o salida) negocia un asignador de la manera habitual. Sin embargo, cuando se conecta el otro pin, es posible que el primer asignador no sea aceptable. En ese caso, el segundo pin elige un asignador diferente y el primer pin se vuelve a conectar mediante el nuevo asignador. Para obtener una implementación de ejemplo, vea [**la clase CTransInPlaceFilter.**](ctransinplacefilter.md)

En el **método ReconnectEx,** filter Graph Manager desconecta y vuelve a conectar los pines de forma asincrónica. El filtro no debe intentar la reconexión a menos **que QueryAccept** devuelva S \_ OK. De lo contrario, el pin se desconectará, lo que provocará errores de grafo. Además, el filtro debe solicitar la reconexión desde dentro del [**método IPin::Conectar,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) en el mismo subproceso. Si el **método Conectar** devuelve en un subproceso, mientras que otro realiza la solicitud de reconexión, el Administrador de filtros Graph podría ejecutar el gráfico antes de realizar la reconexión, lo que provocaría errores de grafo.

 

 



