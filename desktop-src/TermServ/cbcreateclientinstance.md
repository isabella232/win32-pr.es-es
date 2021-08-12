---
title: Función CBCreateClientInstance (Cbclient.h)
description: Crea una instancia del cliente RPC Conexión a Escritorio remoto Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Función CBCreateClientInstance Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b0873fac5b33370333ec8f5774e5b8dbbcd896f6afb9777a6dd74dd6913dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610152"
---
# <a name="cbcreateclientinstance-function"></a>Función CBCreateClientInstance

Crea una instancia del cliente RPC Conexión a Escritorio remoto Broker.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Versión* \[ En\]
</dt> <dd>

Especifica la versión de la interfaz de cliente Conexión a Escritorio remoto Broker que se solicita. Debe ser el siguiente valor.

<dt>

1
</dt> <dd>

Versión 1 del cliente Conexión a Escritorio remoto Broker.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ out\]
</dt> <dd>

Dirección de un puntero de [**interfaz IConnectionBrokerClient**](iconnectionbrokerclient.md) que recibe el Conexión a Escritorio remoto cliente de Broker.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cbclient.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Cbclient.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





