---
description: Firma un hash mediante la clave privada especificada.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Función SslSignHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c57da628aac5c4043abe79491b90bb64d9fa3644199c96ba1e2ad93440f7c11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905624"
---
# <a name="sslsignhash-function"></a>Función SslSignHash

La **función SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) mediante la clave [*privada especificada.*](/windows/desktop/SecGloss/p-gly) El proceso de firma se realiza en el servidor.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia [*del proveedor Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) de seguridad (SSL).

</dd> <dt>

*hPrivateKey* \[ En\]
</dt> <dd>

Identificador de la clave privada que se usará para firmar el hash.

</dd> <dt>

*pbHashValue* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene el hash que se debe firmar.

</dd> <dt>

*cbHashValue* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbHashValue.*

</dd> <dt>

*pbSignature* \[ out\]
</dt> <dd>

Dirección de un búfer que recibe la firma del hash. El *parámetro cbSignature* contiene el tamaño de este búfer. Para determinar el tamaño necesario del búfer, establezca el *parámetro pbSignature* en **NULL.** El tamaño necesario del búfer se devolverá en el *parámetro pwResult.*

</dd> <dt>

*cbSignature* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbSignature.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Puntero a un valor que, tras la finalización, contiene el número real de bytes escritos en el *búfer pbSignature.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

