---
title: MPTHREAT_LOCALIZED_INFO estructura (MpClient. h)
description: Información localizada para una amenaza.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_LOCALIZED_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422284"
---
# <a name="mpthreat_localized_info-structure"></a>MPTHREAT \_ estructura de \_ información localizada

Información localizada para una amenaza.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID. de MPTHREAT**

</dd> <dd>

Identificador de amenaza. El bit superior se establece para identificar las amenazas relacionadas con el antivirus.

</dd> <dt>

**CategoryName**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Clasificación de amenazas, como un troyano o un registrador de virus.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Descripción de la categoría de amenaza.

</dd> <dt>

**SeverityName**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Nivel de gravedad de las amenazas, como grave o moderado.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Descripción del nivel de gravedad de las amenazas.

</dd> <dt>

**ShortDescription**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Breve descripción de la amenaza.

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Nombre de la acción predeterminada, como quitar o poner en cuarentena, sugerida por el motor.

</dd> <dt>

**Advice**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Consejos para la amenaza concreta.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Una dirección URL a una página web que contiene información sobre la amenaza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





