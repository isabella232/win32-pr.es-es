---
description: Ejemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Ejemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161699"
---
# <a name="ball-filter-sample"></a>Ejemplo de filtro de bola

## <a name="description"></a>Descripción

El filtro de bola es un filtro de origen de vídeo que genera una imagen de una bola que salta. En este ejemplo se muestra la negociación de formato y el uso de las clases base de filtro de origen [**CSource**](csource.md) y [**CSourceStream**](csourcestream.md).

El código de Fball.h y Fball.cpp administra las interfaces de filtro. Esos dos archivos contienen aproximadamente el código mínimo necesario para un filtro de código fuente. Los archivos Ball.h y Ball.cpp contienen el código que salta la bola.

Este filtro tiene un único pin de salida, que proporciona una secuencia de vídeo que muestra una bola que salta alrededor del marco. El filtro Ball también acepta solicitudes de administración de calidad del filtro de nivel inferior, que ilustra una estrategia de administración de calidad simple. Este filtro implementa la [**interfaz IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para ese propósito.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: \[ *SDK Root* \] \\ Samples Multimedia DirectShow \\ Filters \\ \\ \\ Ball.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



