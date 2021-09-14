---
title: Función CBCreateClientInstance (Cbclient.h)
description: Crea una instancia del Conexión a Escritorio remoto RPC de Broker.
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
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891329"
---
# <a name="cbcreateclientinstance-function"></a>Función CBCreateClientInstance

Crea una instancia del Conexión a Escritorio remoto RPC de Broker.

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



 

 





