---
description: Se usa para liberar memoria asignada por una de las funciones del proveedor del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Función SslFreeBuffer (Sslprovider. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083432"
---
# <a name="sslfreebuffer-function"></a>SslFreeBuffer función)

La función **SslFreeBuffer** se usa para liberar memoria asignada por una de las funciones del proveedor del [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvInput* \[ de\]
</dt> <dd>

Puntero al búfer de memoria que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *pdwProviderCount* o *ppProviderList* es **null**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

