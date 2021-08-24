---
title: MPCONFIGURATION_DATA estructura (MpClient.h)
description: Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA estructura heredada de Windows environment
- PMPCONFIGURATION_DATA puntero de estructura heredado Windows environment Features
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114585"
---
# <a name="mpconfiguration_data-structure"></a>Estructura DE \_ DATOS MPCONFIGURATION

Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nombre de la configuración que ha cambiado.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de datos usado.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos anteriores, en bytes.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntero a datos anteriores.

</dd> <dt>

**CurrentDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos nuevos, en bytes.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntero a datos nuevos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





