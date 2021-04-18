---
description: Recupera el valor de una propiedad con nombre para un objeto de clave de proveedor del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Función SslGetKeyProperty (Sslprovider. h)
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
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668351"
---
# <a name="sslgetkeyproperty-function"></a>SslGetKeyProperty función)

La función **SslGetKeyProperty** recupera el valor de una propiedad con nombre para un objeto de clave de proveedor del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hKey* \[ de\]
</dt> <dd>

Identificador del proveedor SSL.

</dd> <dt>

*pszProperty* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que contiene el nombre de la propiedad que se va a recuperar. Puede ser uno de los [**identificadores de propiedad de almacenamiento de claves**](key-storage-property-identifiers.md) predefinidos o un identificador de propiedad personalizado.

</dd> <dt>

*ppbOutput* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el valor de propiedad. El autor de la llamada de la función debe liberar este búfer mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbOutput* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>    |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

