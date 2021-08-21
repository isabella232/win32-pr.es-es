---
description: Especifica los atributos de una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cce522403e4b4e416bd3d1ecb9d6c4a551ef3bb67407f853f586bd061f3d8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898952"
---
# <a name="signer_attr_authcode-structure"></a>Estructura SIGNER \_ ATTR \_ AUTHCODE

La **estructura SIGNER \_ ATTR \_ AUTHCODE** especifica los atributos de una [*firma Authenticode.*](../secgloss/a-gly.md)

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño, en bytes, de la estructura .

</dd> <dt>

**fCommercial**
</dt> <dd>

**TRUE** para firmar el asunto como publicador comercial; de lo contrario, **FALSE**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**TRUE** para firmar el asunto como publicador individual; de lo contrario, **FALSE**.

</dd> <dt>

**pwszName**
</dt> <dd>

Nombre para mostrar del archivo tras la descarga.

</dd> <dt>

**pwszInfo**
</dt> <dd>

Nombre para mostrar de la dirección URL del archivo tras la descarga.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE FIRMA \_ DEL \_ FIRMANTE**](signer-signature-info.md)
</dt> </dl>

 

 
