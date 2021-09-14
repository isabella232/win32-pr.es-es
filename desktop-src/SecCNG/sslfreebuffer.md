---
description: Se usa para liberar memoria asignada por una de las funciones de proveedor Capa de sockets seguros protocolo de acceso (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Función SslFreeBuffer (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073616"
---
# <a name="sslfreebuffer-function"></a>Función SslFreeBuffer

La **función SslFreeBuffer** se usa para liberar memoria asignada por una de las [*funciones*](/windows/desktop/SecGloss/s-gly) del proveedor Capa de sockets seguros protocolo de seguridad (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvInput* \[ En\]
</dt> <dd>

Puntero al búfer de memoria que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro pdwProviderCount* o *ppProviderList* es **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

