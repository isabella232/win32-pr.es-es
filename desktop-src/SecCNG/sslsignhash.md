---
description: Firma un hash mediante la clave privada especificada.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Función SslSignHash (Sslprovider. h)
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
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497224"
---
# <a name="sslsignhash-function"></a>SslSignHash función)

La función **SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) mediante la [*clave privada*](/windows/desktop/SecGloss/p-gly)especificada. El proceso de firma se realiza en el servidor.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPrivateKey* \[ de\]
</dt> <dd>

Identificador de la clave privada que se va a utilizar para firmar el hash.

</dd> <dt>

*pbHashValue* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene el hash que se va a firmar.

</dd> <dt>

*cbHashValue* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ enuncia\]
</dt> <dd>

Dirección de un búfer que recibe la firma del hash. El parámetro *cbSignature* contiene el tamaño de este búfer. Para determinar el tamaño del búfer necesario, establezca el parámetro *pbSignature* en **null**. El tamaño necesario del búfer se devolverá en el parámetro *pcbResult* .

</dd> <dt>

*cbSignature* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbSignature* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que, al finalizar, contiene el número real de bytes escritos en el búfer de *pbSignature* .

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

