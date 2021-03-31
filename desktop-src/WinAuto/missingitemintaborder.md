---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791788"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Texto

Este elemento parece ser tabulable, pero no está en el orden de tabulación.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

No se puede tener acceso A un elemento enfocable mediante la navegación de teclado estándar (TAB o Mayús + Tab). Por ejemplo, el elemento no se ha marcado como una posición de tabulación o se le ha asignado un índice de tabulación. Este problema causa problemas para las personas que usan un lector de pantalla y un teclado para la navegación porque:

-   El elemento no es reconocible.
-   Si el elemento es un elemento secundario de un control de lista personalizado, es posible que falten las claves que indican que se puede navegar por el elemento secundario mediante las teclas de dirección o de página.

## <a name="possible-causes"></a>Causas posibles

-   El rol MSAA del elemento o su elemento primario no se ha establecido correctamente. Por ejemplo, si todos los elementos de lista de un control de vista de lista no se exponen a través de MSAA como el sistema de rol \_ \_ ListItem, se produce un error en la comprobación porque no se puede obtener acceso a los elementos de la lista mediante la tecla TAB.
-   El elemento o su elemento primario es un control personalizado que no implementa el tabulador correctamente. Por ejemplo, la propiedad estado de MSAA nunca se establece en estado de \_ foco del sistema \_ .
-   Se seleccionó un elemento que actúa como contenedor de otros elementos para la comprobación pero no admite la navegación por el teclado. Por ejemplo, no se puede tener acceso a una barra de herramientas y a sus elementos secundarios mediante la tecla TAB.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 