---
title: MPTHREAT_DATA estructura (MpClient.h)
description: Datos de notificación pasados debido a la detección o modificación de amenazas.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA estructura heredada de Windows environment
- PMPTHREAT_DATA puntero de estructura Legacy Windows Environment Features
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568717"
---
# <a name="mpthreat_data-structure"></a>Estructura DE DATOS \_ DE MPTHREAT

Datos de notificación pasados debido a la detección o modificación de amenazas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **Id. \_ de MPTHREAT**

</dd> <dd>

Identificador de amenaza. El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sesión asociada a la amenaza. Establezca en -1 si no hay información específica de la sesión disponible.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Acción de amenaza intentada para los **eventos MPNOTIFY \_ THREAT CLEAN \_ \_ SUCCEEDED** / **MPNOTIFY \_ THREAT CLEAN \_ \_ FAILED.**

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado adicional o acciones asociadas a la acción realizada. Se trata de una combinación de marcas de bits de [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MARCA \_ MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**ACCIÓN \_ MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





