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
ms.openlocfilehash: afa9de8ecb598c76daee56367cc9f3ee80a0d0a43f706d11d2eaaa33cd814f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282314"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Estructura DegEngineHistogram

Representa un histograma de una textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Miembros

**horizontalMin**  
Valores mínimos para cada uno de los componentes X, Y, Z y W del eje horizontal (dominio) del histograma.

**horizontalMax**  
Valores máximos para cada uno de los componentes X, Y, Z y W del eje horizontal (dominio) del histograma.

**verticalMin**  
Valores mínimos para cada uno de los componentes X, Y, Z y W del eje vertical (intervalo) del histograma.

**verticalMax**  
Valores máximos para cada uno de los componentes X, Y, Z y W del eje vertical (intervalo) del histograma.

**dataLength**  
Número de muestras que se consideran en el histograma.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



