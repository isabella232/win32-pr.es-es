---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268849"
---
# <a name="toomanychildren"></a>TooManyChildren

## <a name="text"></a>Texto

Se detuvo buscando elementos del mismo nivel adicionales después de encontrar {0} elementos del mismo nivel. Posible árbol incorrecto

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

El árbol de elementos puede ser cíclico y la profundidad de árbol infinita.

Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que especifica lo que parece ser una referencia circular o un bucle infinito.

## <a name="possible-causes"></a>Causas posibles

-   El diseño de la aplicación o el control puede ser demasiado complejo. Esta advertencia puede aparecer para los controles de vista de lista que tienen un gran número de elementos. En estos casos, normalmente puede omitir esta advertencia.
-   Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




