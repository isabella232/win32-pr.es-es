---
description: Recupera el valor de una propiedad con nombre para un objeto de clave de proveedor Capa de sockets seguros protocolo de seguridad (SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Función SslGetKeyProperty (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b86f8a2e76573122bcfcf809d5301bc6bf70690467527f4dc69a5ec12419f56b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906123"
---
# <a name="sslgetkeyproperty-function"></a>Función SslGetKeyProperty

La **función SslGetKeyProperty** recupera el valor de una propiedad con nombre para un [*objeto de clave de*](/windows/desktop/SecGloss/s-gly) proveedor Capa de sockets seguros protocolo de seguridad (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hKey* \[ En\]
</dt> <dd>

Identificador del proveedor SSL.

</dd> <dt>

*pszProperty* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que contiene el nombre de la propiedad que se recuperará. Puede ser uno de los identificadores de propiedad [**Storage clave predefinidos**](key-storage-property-identifiers.md) o un identificador de propiedad personalizado.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el valor de propiedad. El llamador de la función debe liberar este búfer llamando a la [**función SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*output* \[ out\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbOutput.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>    |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

