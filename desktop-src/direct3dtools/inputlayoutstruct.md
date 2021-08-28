---
description: Representa los campos de diseño de entrada de un búfer de vértices, uno por campo en el búfer de vértices.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura InputLayoutStruct
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f5ad2552fe3c0c4b2ebc9919b4bcbd0375d73109
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631393"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span id="vspixengine.inputlayoutstruct"></span>Estructura InputLayoutStruct

Representa los campos de diseño de entrada de un búfer de vértices, uno por campo en el búfer de vértices.

## <a name="syntax"></a>Sintaxis


```C++
} InputLayoutStruct;
```

## <a name="members"></a>Miembros

**SemanticName**  
Cadena COM que contiene el nombre de la semántica asociada.

**SemanticIndex**  
Índice de la semántica asociada.

**Format**  
Formato del campo. Para obtener más información, vea la enumeración \_ DXGI FORMAT.

**InputSlot**  
Ranura de entrada asociada.

**AlignedByteOffset**  

**InputSlotClass**  

**InstanceDataStepRate**  

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



