---
description: Disminuye las referencias al proveedor de protocolo Capa de sockets seguros (SSL).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Función SslDecrementProviderReferenceCount (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: eb2a2f921fd9fa613a5f655449353d42c24897a65f5dc81d6b9321bea961937a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906734"
---
# <a name="ssldecrementproviderreferencecount-function"></a>Función SslDecrementProviderReferenceCount

La **función SslDecrementProviderReferenceCount** disminuye las referencias al [*proveedor de Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo SSL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                        | Descripción                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt> **IDENTIFICADOR \_ DE ESTADO NO \_ VÁLIDO**</dt> <dt>0xC0000008L</dt> </dl> | El identificador del proveedor SSL no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

