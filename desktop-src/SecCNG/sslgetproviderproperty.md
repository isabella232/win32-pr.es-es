---
description: Recupera el valor de una propiedad de proveedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Función SslGetProviderProperty (Sslprovider. h)
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
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912285"
---
# <a name="sslgetproviderproperty-function"></a>SslGetProviderProperty función)

La función **SslGetProviderProperty** recupera el valor de una propiedad de proveedor especificada.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador del proveedor de [*protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) para el que se va a recuperar la propiedad.

</dd> <dt>

*pszProperty* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que contiene el nombre de la propiedad que se va a recuperar.

</dd> <dt>

*ppbOutput* \[ enuncia\]
</dt> <dd>

Dirección de un búfer que recibe el valor de propiedad.

El autor de la llamada de la función debe liberar este búfer mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbOutput* .

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Dirección de un puntero **void** que recibe información de estado de enumeración que se utiliza en las llamadas subsiguientes a esta función. Esta información solo tiene significado para el proveedor SSL y es opaca para el autor de la llamada. El proveedor SSL usa esta información para determinar qué elemento se encuentra a continuación en la enumeración. Si la variable a la que apunta este parámetro contiene **null**, la enumeración se inicia desde el principio.

El autor de la llamada de la función debe liberar esta memoria mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El identificador de *hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

