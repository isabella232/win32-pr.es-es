---
description: Especifica el firmante que se va a firmar.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Estructura de SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666981"
---
# <a name="signer_subject_info-structure"></a>Estructura de \_ información de asunto del firmante \_

La estructura de **\_ \_ información de asunto del firmante** especifica el firmante que se va a firmar.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura, en bytes.

</dd> <dt>

**pdwIndex**
</dt> <dd>

Este miembro está reservado. Debe establecerse en cero.

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

Especifica si el sujeto es un archivo o un [*BLOB*](../secgloss/b-gly.md). Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                         | Significado                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**Firmante \_ \_BLOB de asunto**</dt> <dt>2 (0X2)</dt> </dl> | El asunto es un BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**Firmante \_ \_Archivo de asunto**</dt> <dt>1 (0x1)</dt> </dl> | El asunto es un archivo.<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

Puntero a una estructura de [**\_ \_ información del archivo del firmante**](signer-file-info.md) que especifica el archivo que se va a firmar.

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

Puntero a una estructura de [**\_ \_ información del BLOB del firmante**](signer-blob-info.md) que especifica el BLOB que se va a firmar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
