---
description: Ejemplo de filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Ejemplo de filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677168"
---
# <a name="inftee-filter-sample"></a>Ejemplo de filtro InfTee

## <a name="description"></a>Descripción

El filtro InfTee proporciona una implementación de ejemplo del filtro [tee de PIN infinitos](infinite-pin-tee-filter.md) de DirectShow. El filtro tiene un PIN de entrada y un número dinámico de clavijas de salida. Todos los ejemplos de medios enviados al filtro se entregan simultáneamente desde todos los pin de salida.

Este filtro aparece en GraphEdit bajo el nombre "ejemplo infinita de PIN Tee" para distinguirlo del filtro Tee estándar de PIN infinito que se proporciona en DirectShow.

## <a name="usage"></a>Uso

Dado que este filtro no cambia los datos que recibe, todos los pin deben aceptar el mismo tipo de medio. Durante el proceso de conexión, el filtro podría volver a conectar algunos PIN para que los tipos de medios coincidan.

Los datos que llegan al pin de entrada no se copian antes de que se envíen a los pin de salida. El filtro también garantiza que los datos se entreguen a los filtros de nivel inferior para garantizar que ambas salidas reciben el servicio puntualmente. En concreto, si una de las salidas puede bloquearse en la función miembro [**COutputQueue:: Receive**](coutputqueue-receive.md) , el tee gira un subproceso para entregar el ejemplo. Si no hay ningún subproceso para entregar el ejemplo, el subproceso que entrega el ejemplo al pin de entrada Tee podría pasar los datos a un filtro de nivel inferior; en ese momento, podría bloquearse y mantener los datos del otro filtro de nivel inferior durante largos períodos de tiempo.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ InfTee.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



