---
description: Especifica un BLOB que se firmará.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a865a65b5fd9a1ec658dcc86b1eb2b3dd255804308f04bebf4fffdb0650d71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898932"
---
# <a name="signer_blob_info-structure"></a>ESTRUCTURA DE INFORMACIÓN \_ DE BLOB DE SIGNER \_

\[La **estructura SIGNER \_ BLOB \_ INFO** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **estructura SIGNER \_ BLOB \_ INFO** especifica un [*BLOB*](../secgloss/b-gly.md) que se debe firmar.

> [!Note]  
> Esta estructura no se define en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño, en bytes, de la estructura .

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Puntero a un **GUID que** especifica el paquete de interfaz de sujeto (SIP) que se cargará.

</dd> <dt>

**cbBlob**
</dt> <dd>

Tamaño, en bytes, del BLOB que se firmará.

</dd> <dt>

**pbBlob**
</dt> <dd>

Puntero al BLOB que se firmará.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

Nombre para mostrar del BLOB. Este miembro se puede establecer en **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INFORMACIÓN DEL \_ \_ FIRMANTE**](signer-subject-info.md)
</dt> </dl>

 

 
