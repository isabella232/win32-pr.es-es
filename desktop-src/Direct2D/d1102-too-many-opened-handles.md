---
title: D1102 demasiados identificadores abiertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Se encontró un gran número de interfaces no liberadas. Actualmente hay interfaces no liberadas asignadas por este archivo DLL.
keywords:
- D1102 demasiados identificadores abiertos Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783587"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: demasiados identificadores abiertos

Se encontró un gran número de interfaces no liberadas. Actualmente \[  \] , el número de interfaces no liberadas asignadas por este archivo dll.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*números*
</dt> <dd>

Número de interfaces no liberadas asignadas por este archivo DLL.

</dd> </dl> 

|             |         |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Se creó un gran número de recursos. Aunque Direct2D no tiene ningún límite superior en el número de recursos disponibles (excepto en la memoria), la capa de depuración emite este mensaje informativo cuando encuentra 1001 objetos activos, 2001 objetos activos o 3001 objetos activos, ya que esto podría indicar una fuga en la aplicación.

 

 




