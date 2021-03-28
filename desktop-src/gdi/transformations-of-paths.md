---
description: Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformaciones de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985807"
---
# <a name="transformations-of-paths"></a>Transformaciones de rutas de acceso

Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales. (Si se ha llamado a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , las unidades lógicas son unidades universales; de lo contrario, las unidades lógicas son unidades de página). Una aplicación puede usar transformaciones universales para escalar, girar, distorsionar, trasladar y reflejar las líneas y las curvas de Bézier que definen un trazado.

> [!Note]  
> Una transformación universal dentro de un corchete de ruta de acceso solo afecta a las líneas y curvas dibujadas después de que se haya establecido la transformación. No tendrá ningún efecto en las líneas y curvas dibujadas antes de establecerse. Para obtener una descripción de la transformación universal, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).

 

Una aplicación también puede usar [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para describir la forma del lápiz que se usa para esquematizar un trazado si el lápiz es una pluma geométrica. Para obtener una descripción de los lápices geométricos, consulte [lápices](pens.md).

 

 



