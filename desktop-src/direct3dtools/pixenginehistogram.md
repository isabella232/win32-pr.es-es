---
description: Representa un histograma de una textura.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura DegEngineHistogram
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e6235287d2d87bf6fe1bd79c13813e6bb8500bc3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622171"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Estructura DegEngineHistogram

Representa un histograma de una textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Miembros

**horizontalMin**  
Los valores mínimos para cada uno de los componentes X, Y, Z y W del eje horizontal (dominio) del histograma.

**horizontalMax**  
Valores máximos para cada uno de los componentes X, Y, Z y W del eje horizontal (dominio) del histograma.

**verticalMin**  
Valores mínimos para cada uno de los componentes X, Y, Z y W del eje vertical (intervalo) del histograma.

**verticalMax**  
Valores máximos para cada uno de los componentes X, Y, Z y W del eje vertical (intervalo) del histograma.

**dataLength**  
Número de muestras que se consideran en el histograma.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



