---
description: La estructura EXPERTFRAMEDESCRIPTOR contiene información sobre un marco. Cuando el experto llama correctamente a la función ExpertGetFrame, Monitor de red pasa la estructura EXPERTFRAMEDESCRIPTOR al experto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Estructura EXPERTFRAMEDESCRIPTOR (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a11c131188cdd5230d309a6ff2e39a77ac7886333dafd9860d565fdcb10efc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939032"
---
# <a name="expertframedescriptor-structure"></a>ESTRUCTURA EXPERTFRAMEDESCRIPTOR

La **estructura EXPERTFRAMEDESCRIPTOR** contiene información sobre un marco. Cuando el experto llama correctamente a la función [**ExpertGetFrame,**](expertgetframe.md) Monitor de red pasa la estructura **EXPERTFRAMEDESCRIPTOR** al experto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FrameNumber**
</dt> <dd>

Número de un marco especificado.

</dd> <dt>

**hFrame**
</dt> <dd>

Identificador de un marco.

</dd> <dt>

**pFrame**
</dt> <dd>

Puntero a un marco sin formato.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Tabla que indica dónde identifica cada analizador el inicio de los datos.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Tabla de propiedades de marco que identifica el analizador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el experto especifica FLAGS ATTACH PROPERTIES al llamar a \_ \_ [**ExpertGetFrame**](expertgetframe.md), el **miembro szPropertyText** de cada [**estructura PROPERTYINST**](propertyinst.md) es **NULL.**

Si el experto no especifica FLAGS ATTACH PROPERTIES al llamar a la función \_ \_ [**ExpertGetFrame,**](expertgetframe.md) el miembro **lpPropertyTable** es **NULL en** la devolución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




