---
description: Especifica los atributos de una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Estructura de SIGNER_ATTR_AUTHCODE
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
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003112"
---
# <a name="signer_attr_authcode-structure"></a>\_Estructura fases de atributo de firmante \_

La estructura **Signer \_ ATTR \_ fases** especifica atributos para una firma [*Authenticode*](../secgloss/a-gly.md) .

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

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

Tamaño de la estructura, en bytes.

</dd> <dt>

**fCommercial**
</dt> <dd>

**True** para firmar el sujeto como publicador comercial; en caso contrario, **false**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**True** para firmar el sujeto como publicador individual; en caso contrario, **false**.

</dd> <dt>

**pwszName**
</dt> <dd>

Nombre para mostrar del archivo durante la descarga.

</dd> <dt>

**pwszInfo**
</dt> <dd>

El nombre para mostrar de la dirección URL del archivo durante la descarga.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de \_ firma del firmante \_**](signer-signature-info.md)
</dt> </dl>

 

 
