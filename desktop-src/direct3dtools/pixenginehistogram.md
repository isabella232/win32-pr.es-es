---
description: Representa un histograma de una textura.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineHistogram
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
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152390"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Estructura PixEngineHistogram

Representa un histograma de una textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Miembros

**horizontalMin**  
Los valores mínimos para cada uno de los componentes X, Y, Z y W en el eje horizontal (dominio) del histograma.

**horizontalMax**  
Los valores máximos para cada uno de los componentes X, Y, Z y W en el eje horizontal (dominio) del histograma.

**verticalMin**  
Los valores mínimos para cada uno de los componentes X, Y, Z y W en el eje vertical (intervalo) del histograma.

**verticalMax**  
Los valores máximos para cada uno de los componentes X, Y, Z y W en el eje vertical (intervalo) del histograma.

**dataLength**  
El número de muestras que se consideran en el histograma.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



