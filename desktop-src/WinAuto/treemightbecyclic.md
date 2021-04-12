---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359022"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texto

El árbol tiene {0} niveles de profundidad. Esto podría indicar que el árbol de accesibilidad es cíclico y, por tanto, parecería infinito.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El árbol de elementos es cíclico y la profundidad del árbol puede ser infinita.

Este problema causa problemas para las personas que usan un lector de pantalla y un teclado para la navegación porque no habrá ningún límite aparente en el recorrido de los elementos de la aplicación de destino.

## <a name="possible-causes"></a>Causas posibles

Varios elementos, o sus elementos primarios, son controles personalizados que no implementan el tabulador correctamente. Por ejemplo, la propiedad [Estado](state-property.md) de MSAA no se actualiza correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Directrices de interacción de la experiencia del usuario de Windows: teclado](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 