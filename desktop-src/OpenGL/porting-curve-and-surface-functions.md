---
title: Porting Curve and Surface Functions
description: Porting Curve and Surface Functions
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Porte de IRIS GL, curvas
- porting from IRIS GL,curves
- porting to OpenGL from IRIS GL,curves
- Porte de OpenGL desde IRIS GL, curvas
- Porte de IRIS GL, revisiones de superficie
- porting from IRIS GL,surface patches
- porting to OpenGL from IRIS GL,surface patches
- Porte de OpenGL desde IRIS GL, revisiones de superficie
- curvas
- revisiones de superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed76109bb0067996c26acf48bff7a58773220ad1eb87e13d617bddedeb6d62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777045"
---
# <a name="porting-curve-and-surface-functions"></a>Porting Curve and Surface Functions

OpenGL no admite equivalentes a las funciones GL de IRIS para curvas y revisiones de superficie. Tendrá que volver a escribir el código si incluye cualquiera de las siguientes llamadas:

-   **defbasis**
-   **curvebasis,** **curveprecision,** **crv,** **crvn,** **rcrv,** **rcrvn** y **curveit**
-   **patchbasis,** **patchcurves,** **patchprecision,** **patch** y **rpatch**

En este tema se incluye información sobre lo siguiente.

-   [Porte de objetos DE ASEBS](porting-nurbs-objects.md)
-   [Porte de curvas DE COLORERBS](porting-nurbs-curves.md)
-   [Porte de curvas de recorte](porting-trimming-curves.md)
-   [Porte de superficies DE LA BASE DE DATOS](porting-nurbs-surfaces.md)

 

 




