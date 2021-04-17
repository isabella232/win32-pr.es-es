---
description: Representa información sobre los destinos de llamada para la protección de flujo de control (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO estructura (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677779"
---
# <a name="cfg_call_target_info-structure"></a>\_Estructura de \_ información de destino de llamada cfg \_

Representa información sobre los destinos de llamada para la protección de flujo de control (CFG).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Offset**
</dt> <dd>

Desplazamiento relativo a una dirección virtual (Inicio) proporcionada. Este desplazamiento debe estar alineado con 16 bytes.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas que describen la operación que se va a realizar en la dirección. Si se establece el destino de la **\_ llamada cfg \_ \_ válido** , la dirección se marcará como válida para cfg. De lo contrario, se marcará como destino de llamada no válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




