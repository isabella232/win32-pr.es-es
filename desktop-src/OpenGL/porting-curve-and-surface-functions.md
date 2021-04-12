---
title: Trasladar funciones de curva y superficie
description: Trasladar funciones de curva y superficie
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
- Migración de la contabilidad de IRIS, revisiones de Surface
- portabilidad desde IRIS GL, revisiones de Surface
- trasladar a OpenGL desde IRIS GL, Surface patchs
- Exportación de OpenGL desde IRIS GL, revisiones de Surface
- curvas
- revisiones de Surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356810"
---
# <a name="porting-curve-and-surface-functions"></a>Trasladar funciones de curva y superficie

OpenGL no admite equivalentes a las funciones de GL de IRIS para curvas y revisiones de superficie. Tendrá que volver a escribir el código si incluye cualquiera de las siguientes llamadas:

-   **defbasis**
-   **curvebasis**, **curveprecision**, **CRV**, **crvn**, **rcrv**, **rcrvn** y **curveit**
-   **patchbasis**, **patchcurves**, **patchprecision**, **patch** y **rpatch**

En este tema se incluye información sobre lo siguiente.

-   [Trasladar objetos de NURBS](porting-nurbs-objects.md)
-   [Trasladar curvas de NURBS](porting-nurbs-curves.md)
-   [Trasladar curvas de recorte](porting-trimming-curves.md)
-   [Trasladar superficies NURBS](porting-nurbs-surfaces.md)

 

 




