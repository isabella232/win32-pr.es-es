---
description: Recupera el valor de una propiedad de proveedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Función SslGetProviderProperty (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bfe65fe4033397fd5885eceb3bf0d2ac9ce9aa9b487a84ab7611cb253d979220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906113"
---
# <a name="sslgetproviderproperty-function"></a>Función SslGetProviderProperty

La **función SslGetProviderProperty** recupera el valor de una propiedad de proveedor especificada.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador del proveedor [*Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) de acceso (SSL) para el que se va a recuperar la propiedad .

</dd> <dt>

*pszProperty* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que contiene el nombre de la propiedad que se recuperará.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Dirección de un búfer que recibe el valor de propiedad.

El llamador de la función debe liberar este búfer llamando a la [**función SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*output* \[ out\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbOutput.*

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Dirección de un puntero **VOID** que recibe información de estado de enumeración que se usa en llamadas posteriores a esta función. Esta información solo tiene significado para el proveedor SSL y es opaca para el autor de la llamada. El proveedor SSL usa esta información para determinar qué elemento es el siguiente en la enumeración . Si la variable a la que apunta este parámetro **contiene NULL,** la enumeración se inicia desde el principio.

El llamador de la función debe liberar esta memoria mediante una llamada a la [**función SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *identificador hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

