---
description: Comprueba la firma especificada utilizando el hash proporcionado y la clave pública.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Función SslVerifySignature (Sslprovider. h)
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
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907827"
---
# <a name="sslverifysignature-function"></a>SslVerifySignature función)

La función **SslVerifySignature** comprueba la firma especificada mediante el [*hash*](/windows/desktop/SecGloss/h-gly) proporcionado y la [*clave pública*](/windows/desktop/SecGloss/p-gly).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPublicKey* \[ de\]
</dt> <dd>

Identificador de la clave pública.

</dd> <dt>

*pbHashValue* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene el hash que se va a utilizar para comprobar la firma.

</dd> <dt>

*cbHashValue* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene la firma que se va a comprobar.

</dd> <dt>

*cbSignature* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbSignature* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Windows no llama actualmente a la función **SslVerifySignature** . Esta función es una parte necesaria de la interfaz del proveedor SSL y debe implementarse completamente para garantizar la compatibilidad con versiones posteriores.

Las implementaciones actuales del lado servidor de la conexión del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) llaman a la función [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante la autenticación del cliente para procesar el mensaje de comprobación de certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

