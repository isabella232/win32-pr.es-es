---
description: Contiene una firma de lista de revocación global (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE estructura
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
ms.openlocfilehash: 4d5eec1105e490e68b5fecb46253154b3ed85a112b10641e8394bcc713b71c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059170"
---
# <a name="mf_signature-structure"></a>Estructura \_ MF SIGNATURE

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

Matriz de bytes de tamaño **cbSign** que contiene la firma. El tamaño real de la matriz es mayor que el tamaño especificado en la declaración de estructura.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no se declara en un encabezado del SDK. Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Revocación de certificados de OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estructuras de OPM](opm-structures.md)
</dt> </dl>

 

 




