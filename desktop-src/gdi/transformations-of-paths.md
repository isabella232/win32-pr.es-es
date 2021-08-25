---
description: Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformaciones de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889005"
---
# <a name="transformations-of-paths"></a>Transformaciones de rutas de acceso

Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales. (Si se ha llamado a la función [**SetWorldTransform,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) las unidades lógicas son unidades del mundo; de lo contrario, las unidades lógicas son unidades de página). Una aplicación puede usar transformaciones del mundo para escalar, girar, recortar, traducir y reflejar las líneas y curvas de Bézier que definen un trazado.

> [!Note]  
> Una transformación del mundo dentro de un corchete de trazado solo afecta a las líneas y curvas dibujadas después de establecer la transformación. No tendrá ningún efecto en las líneas y curvas que se dibujaron antes de establecerse. Para obtener una descripción de la transformación del mundo, vea [Espacios de coordenadas y transformaciones.](coordinate-spaces-and-transformations.md)

 

Una aplicación también puede usar [**SetWorldTransform para**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) esquematear la forma del lápiz usado para describir un trazado si el lápiz es un lápiz geométrico. Para obtener una descripción de los lápices geométricos, vea [Lápices](pens.md).

 

 



