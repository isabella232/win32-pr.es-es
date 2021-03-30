---
title: MPCLEAN_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada Clean.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCLEAN_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801921"
---
# <a name="mpclean_data-structure"></a>\_Estructura de datos MPCLEAN

Datos de notificación pasados a la función de devolución de llamada Clean.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID. de MPTHREAT**

</dd> <dd>

Identificador de amenaza para la amenaza de **limpieza de MPNOTIFY \_ \_ \_ Inicio** de MPNOTIFY de la amenaza / **\_ limpia \_ \_ correctamente** / **MPNOTIFY eventos de \_ \_ \_ error de amenaza limpia** . El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **\_ acción MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Acción de amenaza para la amenaza de limpieza de **MPNOTIFY \_ \_ \_ Inicio** de MPNOTIFY de la amenaza / **\_ limpia \_ \_ correctamente** / **MPNOTIFY eventos de \_ \_ \_ error de amenaza limpia** . Consulte [**la \_ acción MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado adicional o acciones asociadas a la acción realizada. Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Información de recursos para los eventos de **\_ \_ \_** / **\_ \_ \_** / **\_ \_ \_ error** de limpieza de amenaza de limpieza de MPNOTIFY de MPNOTIFY correcta Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**\_marca MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_acción MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





