---
title: CHANGE_LOG_HEADER estructura
description: Encabezado del registro de cambios.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER estructura Restaurar sistema
- PCHANGE_LOG_HEADER puntero de estructura Restaurar sistema
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fbfc77aa0d737e43f1174edca2367aeb3b0bfb455b7b70c3de5a24d90214fb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047585"
---
# <a name="change_log_header-structure"></a>Estructura CHANGE \_ LOG \_ HEADER

\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]

Encabezado del registro de cambios.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**RecordHeader**
</dt> <dd>

Estructura [**RECORD \_ HEADER.**](record-header.md) El **miembro dwRecordType** debe establecerse en RecordTypeLogHeader (0). El **miembro dwRecordSize** debe tener en cuenta todos los miembros, además del valor **DWORD** adicional que sigue a este encabezado. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Este miembro debe establecerse en 0xabcdef12.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Este miembro debe establecerse en 2.

</dd> <dt>

**DataHeader**
</dt> <dd>

Estructura [**RECORD \_ HEADER.**](record-header.md) El **miembro dwRecordType** debe establecerse **en RecordTypeVolumePath** (2).

</dd> <dt>

**byteData**
</dt> <dd>

Inicio de una cadena terminada en NULL que especifica la ruta de acceso del volumen.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este encabezado va seguido de un **valor DWORD** que debe ser idéntico al valor del **miembro dwRecordSize** de **RecordHeader.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                       |



 

 





