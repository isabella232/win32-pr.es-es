---
description: Obtiene un identificador hash que se usa para los mensajes de protocolo de enlace hash.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Función SslCreateHandshakeHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666958"
---
# <a name="sslcreatehandshakehash-function"></a>SslCreateHandshakeHash función)

La función **SslCreateHandshakeHash** obtiene un identificador hash que se usa para los mensajes de protocolo de enlace hash.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ enuncia\]
</dt> <dd>

Identificador hash que se puede pasar a otras funciones de proveedor SSL.

</dd> <dt>

*dwProtocol* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

> [!Note]  
> Esta función no se usa con el protocolo SSL 2,0.

 

</dd> <dt>

*dwCipherSuite* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay memoria suficiente para asignar el búfer hash.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El identificador de *hSslProvider* no es válido.<br/>                   |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El valor de *phHandshakeHash* es NULL.<br/>                            |



 

## <a name="remarks"></a>Observaciones

La función **SslCreateHandshakeHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se llama a la función **SslCreateHandshakeHash** para obtener un identificador hash.
2.  A la función [**SslHashHandshake**](sslhashhandshake.md) se le llama cualquier número de veces con el identificador hash para agregar datos al hash.
3.  Se llama a la función [**SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener el Resumen de los datos con hash.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

