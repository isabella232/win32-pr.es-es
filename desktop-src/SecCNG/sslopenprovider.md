---
description: Abre un identificador para el proveedor de protocolos Capa de sockets seguros protocolo (SSL) especificado.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Función SslOpenProvider (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250341"
---
# <a name="sslopenprovider-function"></a>Función SslOpenProvider

La **función SslOpenProvider** abre un identificador para el proveedor de protocolos Capa de sockets seguros [*protocolo*](/windows/desktop/SecGloss/s-gly) (SSL) especificado.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phSslProvider* \[ out\]
</dt> <dd>

Dirección de un **identificador prov de NCRYPT \_ \_** en el que se va a escribir el identificador del proveedor.

Cuando haya terminado de usar el identificador, debe liberarlo llamando a la [**función SslFreeObject.**](sslfreeobject.md)

</dd> <dt>

*pszProviderName* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre del proveedor. Si el valor de este parámetro es **NULL,** se devuelve un identificador para **MS \_ SCHANNEL \_ PROVIDER.**

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro está reservado para su uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                      |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phSslProvider* o *ppProviderList* es **NULL.**<br/> |
| <dl> <dt>**ESTADO \_ NO \_ MEMORY**</dt> <dt>0xC0000017L</dt> </dl>      | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

