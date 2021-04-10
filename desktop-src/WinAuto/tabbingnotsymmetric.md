---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149391"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Texto

Al tabular hacia atrás y hacia delante no se produce el mismo elemento. Esperado {0} pero recibido {1}

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Cuando se usa la navegación de teclado estándar (TAB o Mayús + Tab), no es posible repetir la ruta de acceso del recorrido a través del árbol de elementos del destino de la comprobación si se invierte la dirección de recorrido. Por ejemplo, la tabulación hacia delante (tabulación) x veces desde el elemento a (0) hasta el elemento a (x) y, a continuación, la tabulación hacia atrás (Mayús + Tab) x veces hace que el elemento A (0) vuelva a obtener el foco a través de un conjunto diferente de elementos intermedios.

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque los elementos de recorrido aparecen errático e imprevisibles.

## <a name="possible-causes"></a>Causas posibles

-   Varios elementos o sus elementos primarios son controles personalizados que no implementan el tabulador correctamente. Por ejemplo, la propiedad estado de MSAA no se ha establecido correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 