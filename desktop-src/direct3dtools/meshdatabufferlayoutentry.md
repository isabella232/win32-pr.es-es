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
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282293"
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
Número de componentes homogéneos (valores) que conste de esta entrada.

**isPosition**  
True si la entrada es una posición; de lo contrario, false.

**format**  
Formato de datos de la entrada (registro). Para obtener más información, vea la enumeración REGISTER \_ FORMAT.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



