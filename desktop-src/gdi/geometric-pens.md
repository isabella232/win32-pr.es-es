---
description: Las dimensiones de un lápiz geométrico se especifican en unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Lápices geométricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997365"
---
# <a name="geometric-pens"></a>Lápices geométricos

Las dimensiones de un lápiz geométrico se especifican en unidades lógicas. Por lo tanto, las líneas dibujadas con un lápiz geométrico se pueden escalar, es decir, pueden aparecer más anchas o más estrechas, dependiendo de la transformación universal actual. Para obtener más información sobre la transformación universal, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).

Además de los tres atributos compartidos con los lápices estéticos (ancho, estilo y color), los lápices geométricos poseen los cuatro atributos siguientes: patrón, trama opcional, estilo de extremo y estilo de combinación. Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).

Para crear un lápiz geométrico, una aplicación utiliza la función [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Al igual que con los lápices estéticos, la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) selecciona una plumilla geométrica en el controlador de dominio de la aplicación.

 

 



