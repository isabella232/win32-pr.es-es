---
description: Comprueba la firma especificada mediante el hash y la clave pública proporcionados.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Función SslVerifySignature (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905664"
---
# <a name="sslverifysignature-function"></a>Función SslVerifySignature

La **función SslVerifySignature** comprueba la firma especificada mediante el [*hash proporcionado*](/windows/desktop/SecGloss/h-gly) y la clave [*pública*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia [*del proveedor Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) de protocolo de acceso (SSL).

</dd> <dt>

*hPublicKey* \[ En\]
</dt> <dd>

Identificador de la clave pública.

</dd> <dt>

*pbHashValue* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene el hash que se usará para comprobar la firma.

</dd> <dt>

*cbHashValue* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbHashValue.*

</dd> <dt>

*pbSignature* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene la firma que se va a comprobar.

</dd> <dt>

*cbSignature* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbSignature.*

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



 

## <a name="remarks"></a>Observaciones

La **función SslVerifySignature** no se llama actualmente mediante Windows. Esta función es una parte necesaria de la interfaz del proveedor SSL y debe implementarse por completo para garantizar la compatibilidad con el reenvío.

Las implementaciones actuales del [](/windows/desktop/SecGloss/t-gly) lado servidor de la conexión del protocolo de seguridad de la capa de transporte (TLS) llaman a la función [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante la autenticación del cliente para procesar el mensaje de comprobación del certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

