---
title: Porting Curve and Surface Functions
description: Porting Curve and Surface Functions
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Porte de IRIS GL, curvas
- porting from IRIS GL,curves
- porte a OpenGL desde IRIS GL, curvas
- Porte de OpenGL desde IRIS GL, curvas
- Porte de IRIS GL, revisiones de superficie
- porting from IRIS GL,surface patches
- porting to OpenGL from IRIS GL,surface patches
- Porte de OpenGL desde IRIS GL, revisiones de superficie
- curvas
- revisiones de superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169198"
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
-   [Porting PAPBS Surfaces](porting-nurbs-surfaces.md)

 

 




