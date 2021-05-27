---
title: D1102 Demasiados identificadores abiertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Se encontró un gran número de interfaces no publicados. Actualmente hay interfaces no disponibles asignadas por este archivo DLL.
keywords:
- D1102 Demasiados identificadores abiertos direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548690"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: Demasiados identificadores abiertos

Se encontró un gran número de interfaces no publicados. Actualmente hay número \[ *de* \] interfaces no publicados asignadas por este archivo DLL.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*Número*
</dt> <dd>

Número de interfaces no publicados asignadas por este archivo DLL.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Se creó un gran número de recursos. Aunque Direct2D no tiene ningún límite superior en el número de recursos disponibles (excepto memoria), la capa de depuración emite este mensaje informativo cuando encuentra 1001 objetos en directo, 2001 objetos en directo o 3001 objetos en directo, etc., porque esto podría indicar una pérdida en la aplicación.

 

 




