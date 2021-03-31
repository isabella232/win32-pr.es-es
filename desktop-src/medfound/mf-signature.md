---
description: Contiene una firma de lista de revocación global (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Estructura de MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278923"
---
# <a name="mf_signature-structure"></a>\_Estructura de firma MF

Contiene una firma de lista de revocación global (GRL).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSignVer**
</dt> <dd>

Número de versión de la firma.

</dd> <dt>

**cbSign**
</dt> <dd>

Tamaño de la firma en bytes.

</dd> <dt>

**rgSign**
</dt> <dd>

Matriz de bytes de tamaño **cbSign** que contiene la firma. El tamaño real de la matriz es mayor que el tamaño especificado en la declaración de la estructura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no se declara en un encabezado de SDK. Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Revocación de certificados OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estructuras OPM](opm-structures.md)
</dt> </dl>

 

 




