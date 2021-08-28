---
description: Representa información sobre una sola entrada en el diseño del búfer de una malla.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 40360e73f480b4c12dcb24311c26fd9718093705
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625361"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry (estructura)

Representa información sobre una sola entrada en el diseño del búfer de una malla.

## <a name="syntax"></a>Sintaxis


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Miembros

**pName**  
Cadena COM que contiene el nombre de la entrada.

**numComponents**  
El número de componentes homogéneos (valores) que forma esta entrada.

**isPosition**  
True si la entrada es una posición; de lo contrario, false.

**format**  
Formato de datos de la entrada (registro). Para obtener más información, vea la enumeración REGISTER \_ FORMAT.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



