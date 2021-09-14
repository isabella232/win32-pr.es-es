---
title: Directrices de rendimiento
description: Directrices para desarrollar aplicaciones que tienen un buen rendimiento en Servicios de Escritorio remoto entorno.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968000"
---
# <a name="performance-guidelines"></a>Directrices de rendimiento

En las secciones siguientes se proporcionan directrices para desarrollar aplicaciones que tienen un buen rendimiento en un Servicios de Escritorio remoto trabajo.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Efectos gráficos](graphic-effects.md)
</dt> <dd>

Lista de características que se deben deshabilitar al ejecutarse como una sesión remota en un Servicios de Escritorio remoto remoto.

</dd> <dt>

[Directrices para tareas en segundo plano en Servicios de Escritorio remoto](background-tasks.md)
</dt> <dd>

Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecuten en un entorno Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consumen muchos recursos.

</dd> <dt>

[Uso de subprocesos](thread-usage.md)
</dt> <dd>

Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno multiusuario Servicios de Escritorio remoto procesador.

</dd> <dt>

[Detección del Servicios de Escritorio remoto de datos](detecting-the-terminal-services-environment.md)
</dt> <dd>

Para optimizar el rendimiento, es un procedimiento recomendado que las aplicaciones detecten si se ejecutan en una sesión Servicios de Escritorio remoto cliente.

</dd> </dl>

Compruebe la aplicación en busca de pérdidas de memoria y resuelva los problemas. Por supuesto, este es un buen consejo para cualquier aplicación, pero en un entorno de Servicios de Escritorio remoto, varios usuarios pueden ejecutar una aplicación varias veces, lo que aumenta rápidamente el efecto de una pérdida de memoria.

Las animaciones, las imágenes grandes, el audio y otros servicios que consumen mucho ancho de banda deben configurarse. Cuando estos servicios no son la función principal, pueden estar desactivados de forma predeterminada para las sesiones remotas, pero se habilitan cuando una sesión se ejecuta localmente o a través de una conexión de ancho de banda alto. Si el propósito de una aplicación es proporcionar servicios de alto ancho de banda, como las difusiones de vídeo de streaming, el servicio no tiene que estar desactivado de forma predeterminada.

 

 




