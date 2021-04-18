---
title: Función CBCreateClientInstance (Cbclient. h)
description: Crea una instancia del cliente RPC de Conexión a Escritorio remoto Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función CBCreateClientInstance
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681232"
---
# <a name="cbcreateclientinstance-function"></a>CBCreateClientInstance función)

Crea una instancia del cliente RPC de Conexión a Escritorio remoto Broker.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Versión* \[ de de\]
</dt> <dd>

Especifica la versión de la interfaz de cliente de Conexión a Escritorio remoto Broker que se solicita. Debe ser el siguiente valor.

<dt>

1
</dt> <dd>

Versión 1 del cliente del agente de Conexión a Escritorio remoto.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ enuncia\]
</dt> <dd>

Dirección de un puntero de interfaz [**IConnectionBrokerClient**](iconnectionbrokerclient.md) que recibe el objeto de cliente de conexión a escritorio remoto Broker.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Cbclient. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





