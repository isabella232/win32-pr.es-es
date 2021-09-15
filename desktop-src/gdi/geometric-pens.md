---
description: Las dimensiones de un lápiz geométrico se especifican en unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Lápices geométricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570684"
---
# <a name="geometric-pens"></a>Lápices geométricos

Las dimensiones de un lápiz geométrico se especifican en unidades lógicas. Por lo tanto, las líneas dibujadas con un lápiz geométrico se pueden escalar, es decir, pueden parecer más anchas o más estrechas, en función de la transformación del mundo actual. Para obtener más información sobre la transformación del mundo, vea [Espacios de coordenadas y transformaciones.](coordinate-spaces-and-transformations.md)

Además de los tres atributos compartidos con lápices de color (ancho, estilo y color), los lápices geométricos poseen los cuatro atributos siguientes: patrón, sombreado opcional, estilo final y estilo de combinación. Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).

Para crear un lápiz geométrico, una aplicación usa la [**función ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Al igual que con los lápices de geometría, la [**función SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) selecciona un lápiz geométrico en el controlador de dominio de la aplicación.

 

 



