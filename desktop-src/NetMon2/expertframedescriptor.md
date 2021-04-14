---
description: La estructura EXPERTFRAMEDESCRIPTOR contiene información sobre un marco. Cuando el experto llama a la función ExpertGetFrame correctamente, Monitor de red pasa la estructura EXPERTFRAMEDESCRIPTOR al experto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Estructura EXPERTFRAMEDESCRIPTOR (Netmon. h)
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
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497008"
---
# <a name="expertframedescriptor-structure"></a>Estructura EXPERTFRAMEDESCRIPTOR

La estructura **EXPERTFRAMEDESCRIPTOR** contiene información sobre un marco. Cuando el experto llama a la función [**ExpertGetFrame**](expertgetframe.md) correctamente, monitor de red pasa la estructura **EXPERTFRAMEDESCRIPTOR** al experto.

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

**Númeromarco**
</dt> <dd>

Número de un marco especificado.

</dd> <dt>

**hFrame**
</dt> <dd>

Identificador de un marco.

</dd> <dt>

**pFrame**
</dt> <dd>

Puntero a un fotograma sin formato.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Tabla que indica la ubicación en la que cada analizador identifica el inicio de los datos.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Tabla de propiedades de marco que identifica el analizador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el experto especifica FLAGs \_ Attach \_ Properties al llamar a [**ExpertGetFrame**](expertgetframe.md), el miembro **szPropertyText** de cada estructura [**PROPERTYINST**](propertyinst.md) es **null**.

Si el experto no especifica \_ las propiedades de adjuntar marcas \_ al llamar a la función [**ExpertGetFrame**](expertgetframe.md) , el miembro **lpPropertyTable** es **null** en la devolución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




