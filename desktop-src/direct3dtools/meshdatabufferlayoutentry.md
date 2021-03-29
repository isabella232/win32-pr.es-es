---
description: Representa información sobre una única entrada en el diseño de búfer de una malla.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura MeshDataBufferLayoutEntry
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
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806830"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Estructura MeshDataBufferLayoutEntry

Representa información sobre una única entrada en el diseño de búfer de una malla.

## <a name="syntax"></a>Sintaxis


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Miembros

**pName**  
Cadena COM que contiene el nombre de la entrada.

**numComponents**  
El número de componentes homogéneos (valores) que componen esta entrada.

**isPosition**  
True si la entrada es una posición; en caso contrario, false.

**format**  
El formato de datos de la entrada (registro). Para obtener más información, consulte la \_ enumeración de formato de registro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



