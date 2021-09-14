---
description: Contiene información sobre un proveedor de servicios criptográficos (CSP) de tarjeta inteligente.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073775"
---
# <a name="kerb_smartcard_csp_info-structure"></a>Estructura DE \_ INFORMACIÓN de CSP de TARJETA INTELIGENTE \_ \_ KERB

La **estructura KERB \_ SMARTCARD CSP \_ \_ INFO** contiene información sobre un proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) de tarjeta inteligente.

Esta estructura no se declara en un encabezado público.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

Tamaño, en bytes, de esta estructura, incluidos los datos anexados.

</dd> <dt>

**MessageType**
</dt> <dd>

Tipo de mensaje que se pasa. Este miembro debe establecerse en 1.

</dd> <dt>

**ContextInformation**
</dt> <dd>

Reservado.

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

Reservado.

</dd> <dt>

**flags**
</dt> <dd>

Reservado.

</dd> <dt>

**KeySpec**
</dt> <dd>

Clave privada que se va a usar desde el contenedor de claves especificado en el búfer **bBuffer**. La clave puede ser uno de los siguientes valores, definidos en WinCrypt.h.



| Value                                                                                                                                                                                                                   | Significado                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> <dt>1</dt> </dl> | La clave es una clave de intercambio de claves.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ FIRMA**</dt> <dt>2</dt> </dl>       | La clave es una clave de firma.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

Número de caracteres del búfer **bBuffer** que preceden al nombre de la tarjeta inteligente en ese búfer.

> [!IMPORTANT]
> Si no se proporciona el nombre de la tarjeta inteligente, el búfer debe contener una cadena vacía.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

Número de caracteres del búfer **bBuffer** que preceden al nombre del lector de tarjetas inteligentes en ese búfer.

> [!IMPORTANT]
> Si no se proporciona el nombre del lector de tarjetas inteligentes, el búfer debe contener una cadena vacía.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

Número de caracteres del búfer **bBuffer** que preceden al nombre del contenedor de claves en ese búfer. Esta cadena no puede estar vacía.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

Número de caracteres del búfer **bBuffer** que preceden al nombre del CSP en ese búfer.

</dd> <dt>

**bBuffer**
</dt> <dd>

Matriz de caracteres inicializada en una longitud de `sizeof(DWORD)` . Este búfer contiene los nombres a los que hacen referencia los miembros **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** y **nCSPNameOffset,** así como los datos adicionales proporcionados por el CSP.

Los nombres que no se proporcionan deben representarse en este búfer mediante cadenas vacías.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se serializa esta estructura, los miembros de la estructura deben estar alineados con límites que son múltiplo de 2 bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INICIO DE \_ SESIÓN DE CERTIFICADO \_ KERB**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
