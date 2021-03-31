---
title: Directrices de rendimiento
description: Directrices para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419120"
---
# <a name="performance-guidelines"></a>Directrices de rendimiento

En las secciones siguientes se proporcionan instrucciones para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Efectos gráficos](graphic-effects.md)
</dt> <dd>

Una lista de características que deben deshabilitarse cuando se ejecuta como una sesión remota en un entorno de Servicios de Escritorio remoto.

</dd> <dt>

[Instrucciones para tareas en segundo plano en Servicios de Escritorio remoto](background-tasks.md)
</dt> <dd>

Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecute en un entorno de Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consuman muchos recursos.

</dd> <dt>

[Uso de subprocesos](thread-usage.md)
</dt> <dd>

Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador.

</dd> <dt>

[Detección del entorno de Servicios de Escritorio remoto](detecting-the-terminal-services-environment.md)
</dt> <dd>

Para optimizar el rendimiento, es recomendable que las aplicaciones detecten si se ejecutan en una sesión de cliente Servicios de Escritorio remoto.

</dd> </dl>

Compruebe si hay pérdidas de memoria en la aplicación y resuelva los problemas. Por supuesto, esto es un buen consejo para cualquier aplicación, pero en un entorno de Servicios de Escritorio remoto, una aplicación se puede ejecutar varias veces por varios usuarios, lo que aumenta rápidamente el efecto de una fuga de memoria.

Las animaciones, imágenes de gran tamaño, audio y otros servicios con un uso intensivo de ancho de banda deben ser configurables. Cuando estos servicios no son la función principal, pueden desactivarse de forma predeterminada para las sesiones remotas, pero se habilitan cuando una sesión se ejecuta localmente o a través de una conexión de ancho de banda alto. Si el propósito de una aplicación es proporcionar servicios de gran ancho de banda, como la transmisión por secuencias de vídeo, el servicio no tiene que estar desactivado de forma predeterminada.

 

 




