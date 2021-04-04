---
description: Ejemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Ejemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906823"
---
# <a name="ball-filter-sample"></a>Ejemplo de filtro de bola

## <a name="description"></a>Descripción

El filtro de bola es un filtro de origen de vídeo que genera una imagen de una bola de rebote. Este ejemplo muestra la negociación de formato y el uso de las clases base de filtro de origen [**CSource**](csource.md) y [**CSourceStream**](csourcestream.md).

El código de Fball. h y Fball. cpp administra las interfaces de filtro. Estos dos archivos contienen aproximadamente el código mínimo necesario para un filtro de origen. Los archivos Ball. h y Ball. cpp contienen el código que rebota la bola.

Este filtro tiene un solo PIN de salida, que proporciona un flujo de vídeo que muestra una bola que rebota en el fotograma. El filtro Ball también acepta solicitudes de administración de calidad del filtro de nivel inferior, lo que muestra una estrategia de administración de calidad simple. Este filtro implementa la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para ese propósito.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: \[ ejemplos *raíz de SDK* \] \\ ejemplo de filtros de DirectShow de \\ multimedia \\ \\ \\ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



