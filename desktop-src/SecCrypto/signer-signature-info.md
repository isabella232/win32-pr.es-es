---
description: Contiene información sobre una firma digital.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: SIGNER_SIGNATURE_INFO estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3dc76db36cd752e22bbcd4d2f6672f7359dad882346b764fef0f4d12ef0901f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973399"
---
# <a name="signer_signature_info-structure"></a>Estructura SIGNER \_ SIGNATURE \_ INFO

La **estructura SIGNER \_ SIGNATURE \_ INFO** contiene información sobre una firma digital.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño, en bytes, de la estructura .

</dd> <dt>

**algidHash**
</dt> <dd>

Algoritmo hash utilizado para la firma digital.

</dd> <dt>

**dwAttrChoice**
</dt> <dd>

Especifica si la firma tiene atributos [*Authenticode.*](../secgloss/a-gly.md) Este miembro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                      | Significado                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**SIGNER \_ AUTHCODE \_ ATTR**</dt> <dt>1</dt> </dl> | La firma tiene [*atributos Authenticode.*](../secgloss/a-gly.md)<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**SIGNER \_ NO \_ ATTR**</dt> <dt>0</dt> </dl>                   | La firma no tiene atributos [*Authenticode.*](../secgloss/a-gly.md)<br/> |



 

</dd> <dt>

**pAttrAuthcode**
</dt> <dd>

Especifica los atributos de una [*firma Authenticode.*](../secgloss/a-gly.md) Este miembro es necesario si el valor del **miembro dwAttrChoice** es **SIGNER \_ AUTHCODE \_ ATTR**.

</dd> <dt>

**psAuthenticated**
</dt> <dd>

Atributos proporcionados por el usuario autenticados agregados a la firma digital.

</dd> <dt>

**psUnauthenticated**
</dt> <dd>

Atributos proporcionados por el usuario no autenticados agregados a la firma digital.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
