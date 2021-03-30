---
title: MPCONFIGURATION_DATA estructura (MpClient. h)
description: Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCONFIGURATION_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079223"
---
# <a name="mpconfiguration_data-structure"></a>\_Estructura de datos MPCONFIGURATION

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

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Nombre de la configuración que cambió.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El tipo de datos utilizado.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos anteriores, en bytes.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Tipo: **byte \** _

</dd> <dd>

Puntero a los datos anteriores.

</dd> <dt>

_ *CurrentDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos nuevos, en bytes.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Tipo: **byte \***

</dd> <dd>

Puntero a los nuevos datos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





