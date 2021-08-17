---
description: Enumeración de dispositivos y filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumeración de dispositivos y filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401779"
---
# <a name="enumerating-devices-and-filters"></a>Enumeración de dispositivos y filtros

A veces, una aplicación debe buscar un filtro determinado en el sistema del usuario. Por ejemplo, una aplicación de captura de vídeo podría mostrar una lista de dispositivos de captura disponibles. Dado DirectShow utiliza una arquitectura basada en componentes, no puede saber en tiempo de diseño qué filtros están instalados en el sistema del usuario. Esto es especialmente cierto para los filtros que representan dispositivos de hardware. DirectShow proporciona dos componentes que localizan filtros registrados:

-   El [enumerador de dispositivos del](system-device-enumerator.md) sistema busca filtros por su categoría.
-   El [Asignador de filtros](filter-mapper.md) busca filtros según los criterios de búsqueda proporcionados por la aplicación.

Los enumeradores que se de analizan en esta sección siguen el formato estándar que usan las interfaces de enumeración COM. Para obtener más información, vea el tema "IEnumXXXX" en el Kit de desarrollo de software (SDK) de la plataforma de Microsoft.

Esta sección contiene los siguientes temas:

-   [Uso del enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)
-   [Uso del asignador de filtros](using-the-filter-mapper.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> </dl>

 

 



