---
description: Abre un identificador para el proveedor de protocolo de protocolo de Capa de sockets seguros (SSL) especificado.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Función SslOpenProvider (Sslprovider. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275323"
---
# <a name="sslopenprovider-function"></a>SslOpenProvider función)

La función **SslOpenProvider** abre un identificador para el proveedor de protocolo de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) especificado.

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

*phSslProvider* \[ enuncia\]
</dt> <dd>

Dirección de un **identificador de \_ Prov \_ de NCRYPT** en el que se va a escribir el identificador del proveedor.

Cuando haya terminado de usar el identificador, debe liberarlo llamando a la función [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pszProviderName* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre del proveedor. Si el valor de este parámetro es **null**, se devuelve un identificador **al \_ \_ proveedor de MS Schannel** .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro está reservado para un uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                      |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phSslProvider* o *ppProviderList* es **null**.<br/> |
| <dl> <dt>**Estado \_ de NO hay \_ memoria**</dt> <dt>0xC0000017L</dt> </dl>      | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

