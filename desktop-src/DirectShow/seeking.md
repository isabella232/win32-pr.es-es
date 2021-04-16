---
description: Invoca
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Invoca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104567136"
---
# <a name="seeking"></a>Invoca

Los filtros admiten la búsqueda a través de la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . La aplicación consulta el administrador de gráficos de filtro para **IMediaSeeking** y lo usa para emitir comandos de búsqueda. Filter Graph Manager distribuye cada comando de búsqueda a todos los filtros de representación del gráfico. Cada representador pasa el comando ascendente, a través de los terminales de salida de los filtros de nivel superior, hasta que alcanza un filtro que puede ejecutar la búsqueda. Normalmente, un filtro de origen o un filtro de analizador, como el [divisor de AVI](avi-splitter-filter.md), lleva a cabo la operación de búsqueda.

Cuando un filtro realiza una operación de búsqueda, vacía los datos pendientes. El resultado es minimizar la latencia de los comandos de búsqueda, ya que los datos existentes se vacían del gráfico. Después de un comando de búsqueda, el tiempo de secuencia se restablece en cero.

En el diagrama siguiente se muestra la secuencia de eventos.

![secuencia de eventos](images/seeking.png)

Si un filtro de analizador tiene más de un PIN de salida, normalmente designa uno de ellos para que acepte comandos de búsqueda. Los demás PIN rechazan u omiten cualquier comando de búsqueda que reciban. De esta manera, el analizador mantiene todas sus secuencias sincronizadas. Sin embargo, todos los pin de salida deben implementar [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) y [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) para devolver las capacidades de búsqueda del filtro. Esto garantiza que el administrador de gráficos de filtro devuelva el valor correcto a la aplicación.

La interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) está en desuso para los filtros. Los clientes de automatización todavía necesitan usar esta interfaz en el administrador de gráficos de filtro, porque **IMediaSeeking** no es compatible con automatización, pero el administrador de gráficos de filtros traduce todas las llamadas a **IMediaPosition** en llamadas **IMediaSeeking** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vaciar](flushing.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



