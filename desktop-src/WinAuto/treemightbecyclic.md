---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614445"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texto

El árbol tiene {0} niveles de profundidad. Esto podría indicar que el árbol de accesibilidad es cíclico y, por tanto, parecería infinito.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El árbol de elementos es cíclico y la profundidad del árbol podría ser infinita.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque no habrá ningún límite aparente para el recorrido de elementos en la aplicación de destino.

## <a name="possible-causes"></a>Causas posibles

Varios elementos, o sus elementos principales, son controles personalizados que no implementan tabulación correctamente. Por ejemplo, la propiedad MSAA [State](state-property.md) no se actualiza correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Instrucciones de interacción de la experiencia del usuario: teclado](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 