---
description: Especifica un BLOB que se va a firmar.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Estructura de SIGNER_BLOB_INFO
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
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547078"
---
# <a name="signer_blob_info-structure"></a>Estructura de \_ información del BLOB del firmante \_

\[La estructura de **\_ \_ información del BLOB del firmante** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La estructura de **\_ \_ información del BLOB del firmante** especifica el [*BLOB*](../secgloss/b-gly.md) que se va a firmar.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

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

Tamaño de la estructura, en bytes.

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Un puntero a un **GUID** que especifica el paquete de interfaz de sujeto (SIP) que se va a cargar.

</dd> <dt>

**cbBlob**
</dt> <dd>

Tamaño, en bytes, del BLOB que se va a firmar.

</dd> <dt>

**pbBlob**
</dt> <dd>

Puntero al BLOB que se va a firmar.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

Nombre para mostrar del BLOB. Este miembro se puede establecer en **null**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de \_ asunto del firmante \_**](signer-subject-info.md)
</dt> </dl>

 

 
