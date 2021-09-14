---
title: MPCLEAN_DATA estructura (MpClient.h)
description: Datos de notificación pasados a la función de devolución de llamada limpia.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA estructura heredada de Windows environment
- PMPCLEAN_DATA puntero de estructura heredados Windows environment features
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170226"
---
# <a name="mpclean_data-structure"></a>Estructura DE \_ DATOS MPCLEAN

Datos de notificación pasados a la función de devolución de llamada limpia.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **Id. \_ de MPTHREAT**

</dd> <dd>

Identificador de amenaza para los **eventos MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Acción de amenaza para los **eventos MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Vea [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado adicional o acciones asociadas a la acción realizada. Se trata de una combinación de marcas de bits de [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Información de recursos para los eventos **MPNOTIFY \_ CLEAN \_ THREAT \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> <dt>

[**MARCA \_ MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**ACCIÓN \_ MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





