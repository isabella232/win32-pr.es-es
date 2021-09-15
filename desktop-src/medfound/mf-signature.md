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
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474123"
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



## <a name="members"></a>Members

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

## <a name="remarks"></a>Observaciones

Esta estructura no se declara en un encabezado sdk. Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Revocación de certificados de OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estructuras de OPM](opm-structures.md)
</dt> </dl>

 

 




