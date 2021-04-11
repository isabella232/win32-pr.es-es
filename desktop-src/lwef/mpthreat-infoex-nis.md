---
title: MPTHREAT_INFOEX_NIS estructura (MpClient. h)
description: Contiene información específica de NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_NIS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079320"
---
# <a name="mpthreat_infoex_nis-structure"></a>MPTHREAT \_ INFOEX ( \_ estructura de NIS)

Contiene información específica de NIS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SourceIP**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd></dd> <dt>

**DestinationIP**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd></dd> <dt>

**dwSourceport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**dwDestinationport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**Protocolo**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd></dd> <dt>

**Vínculo**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





