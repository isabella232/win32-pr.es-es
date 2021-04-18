---
title: MPTHREAT_DATA estructura (MpClient. h)
description: Datos de notificación pasados debido a la detección de amenazas o a la modificación.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714643"
---
# <a name="mpthreat_data-structure"></a>\_Estructura de datos MPTHREAT

Datos de notificación pasados debido a la detección de amenazas o a la modificación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID. de MPTHREAT**

</dd> <dd>

Identificador de amenaza. El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sesión asociada a la amenaza. Establézcalo en-1 si no hay disponible ninguna información específica de la sesión.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **\_ acción MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Se intentó una acción de amenaza para los eventos de **\_ \_ \_** / **\_ \_ \_ error al limpiar** la amenaza de MPNOTIFY correctamente MPNOTIFY.

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado adicional o acciones asociadas a la acción realizada. Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_marca MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_acción MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





