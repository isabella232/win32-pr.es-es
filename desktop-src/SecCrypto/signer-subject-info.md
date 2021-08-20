---
description: Especifica un sujeto para firmar.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: SIGNER_SUBJECT_INFO estructura
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
ms.openlocfilehash: 418eacfaf654efb487dc61f692b1d384e045d62f9fc8f9af96f2fd746810440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973223"
---
# <a name="signer_subject_info-structure"></a>Signer \_ SUBJECT \_ INFO (estructura)

La **estructura SIGNER \_ SUBJECT \_ INFO** especifica un sujeto para firmar.

> [!Note]  
> Esta estructura no se define en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

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

Tamaño, en bytes, de la estructura .

</dd> <dt>

**pdwIndex**
</dt> <dd>

Este miembro está reservado. Debe establecerse en cero.

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

Especifica si el asunto es un archivo o un [*BLOB.*](../secgloss/b-gly.md) Este miembro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                         | Significado                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**FIRMANTE \_ SUBJECT \_ BLOB**</dt> <dt>2 (0x2)</dt> </dl> | El asunto es un BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**FIRMANTE \_ ARCHIVO \_ DE ASUNTO**</dt> <dt>1 (0x1)</dt> </dl> | El asunto es un archivo.<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

Puntero a una estructura [**SIGNER \_ FILE \_ INFO**](signer-file-info.md) que especifica el archivo que se debe firmar.

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

Puntero a una estructura [**SIGNER \_ BLOB \_ INFO**](signer-blob-info.md) que especifica el BLOB que se debe firmar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
