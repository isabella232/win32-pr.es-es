---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc8e413c12b93ebcb3fcbb9d38e56041bedf4e0b8abb98581d77fae4c275f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071815"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Texto

Este elemento parece que se puede tabular, pero no está en el orden de tabulación.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

No se puede acceder a un elemento que se pueda centrar mediante la navegación con el teclado estándar (Tab o Mayús+Tab). Por ejemplo, el elemento no se ha marcado como un punto de tabulación ni se le ha asignado un índice de tabulación. Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque:

-   El elemento no se puede detectar.
-   Si el elemento es un elemento secundario de un control de lista personalizado, pueden faltar indicaciones que indiquen que el elemento secundario se puede navegar mediante las teclas Arrow o Page.

## <a name="possible-causes"></a>Causas posibles

-   El rol MSAA del elemento o su elemento primario no se establece correctamente. Por ejemplo, si todos los elementos de lista de un control de vista de lista no se exponen a través de MSAA como ROLE SYSTEM LISTITEM, se produce un error en la comprobación porque los elementos de lista no son accesibles mediante la tecla \_ \_ Tab.
-   El elemento o su elemento primario es un control personalizado que no implementa correctamente el tabulador. Por ejemplo, la propiedad MSAA State nunca se establece en STATE \_ SYSTEM \_ FOCUSABLE.
-   Se seleccionó un elemento que actúa como contenedor para otros elementos para la comprobación, pero no admite la propia navegación con el teclado. Por ejemplo, una barra de herramientas y sus elementos secundarios no son accesibles mediante la tecla TAB.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 