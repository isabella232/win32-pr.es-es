---
description: Enumerar dispositivos y filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerar dispositivos y filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906758"
---
# <a name="enumerating-devices-and-filters"></a>Enumerar dispositivos y filtros

A veces, una aplicación necesita buscar un filtro determinado en el sistema del usuario. Por ejemplo, una aplicación de captura de vídeo puede mostrar una lista de dispositivos de captura disponibles. Dado que DirectShow usa una arquitectura basada en componentes, no puede saber en tiempo de diseño qué filtros están instalados en el sistema del usuario. Esto es especialmente cierto para los filtros que representan dispositivos de hardware. DirectShow proporciona dos componentes que buscan los filtros registrados:

-   El [enumerador de dispositivos del sistema](system-device-enumerator.md) busca filtros por su categoría.
-   El [asignador de filtros](filter-mapper.md) busca filtros según los criterios de búsqueda proporcionados por la aplicación.

Los enumeradores descritos en esta sección siguen el formato estándar que utilizan las interfaces de enumeración COM. Para obtener más información, vea el tema "IEnumXXXX" en el kit de desarrollo de software (SDK) de la plataforma de Microsoft.

Esta sección contiene los siguientes temas:

-   [Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)
-   [Usar el asignador de filtros](using-the-filter-mapper.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



