---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6bda8de3e07f0ac6be3aa3a2a7bd750508dead1f5c2662391a056b258b36d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644105"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Texto

El tabulador hacia atrás y hacia delante no produce el mismo elemento. Se esperaba {0} pero se recibió {1}

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Cuando se usa la navegación con el teclado estándar (Tab o Mayús+Tab), no es posible repetir la ruta de acceso del recorrido a través del árbol de elementos del destino de comprobación si se invierte la dirección del recorrido. Por ejemplo, la tabulación hacia delante (Tab) x veces del elemento A(0) al elemento A(x) y, a continuación, la tabulación hacia atrás (Mayús+Tab) x veces hace que el elemento A(0) recupere el foco a través de un conjunto diferente de elementos intermedios.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque los elementos de recorrido parecen erráticos e impredecibles.

## <a name="possible-causes"></a>Causas posibles

-   Varios elementos o sus elementos principales son controles personalizados que no implementan correctamente la tabulación. Por ejemplo, la propiedad MSAA State no está establecida correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 