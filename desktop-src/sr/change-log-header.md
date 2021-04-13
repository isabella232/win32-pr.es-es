---
title: Estructura de CHANGE_LOG_HEADER
description: Encabezado del registro de cambios.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restaurar sistema de estructura CHANGE_LOG_HEADER
- PCHANGE_LOG_HEADER de puntero de estructura para restaurar sistema
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421981"
---
# <a name="change_log_header-structure"></a>CAMBIAR \_ la \_ estructura del encabezado del registro

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

Una estructura de [**\_ encabezado de registro**](record-header.md) . El miembro **dwRecordType** debe establecerse en RecordTypeLogHeader (0). El miembro **dwRecordSize** debe tener en cuenta todos los miembros, más el valor **DWORD** adicional que sigue a este encabezado. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Este miembro debe establecerse en 0xabcdef12.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Este miembro debe establecerse en 2.

</dd> <dt>

**MyHeader**
</dt> <dd>

Una estructura de [**\_ encabezado de registro**](record-header.md) . El miembro **dwRecordType** debe establecerse en **RecordTypeVolumePath** (2).

</dd> <dt>

**byteData**
</dt> <dd>

Inicio de una cadena terminada en null que especifica la ruta de acceso del volumen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este encabezado va seguido de un valor **DWORD** que debe ser idéntico al valor del miembro **dwRecordSize** de **RecordHeader**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                       |



 

 





