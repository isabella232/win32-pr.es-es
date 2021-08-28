---
title: Interfaz IConnectionBrokerRequest (Cbclient.h)
description: Proporciona los métodos necesarios para obtener los resultados del método asincrónico IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Interfaz IConnectionBrokerRequest Servicios de Escritorio remoto
- Interfaz IConnectionBrokerRequest Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dfc858e16371ec44ef965722c0d37bd388b060ce4d7ce75adbd904074df03b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059143"
---
# <a name="iconnectionbrokerrequest-interface"></a>Interfaz IConnectionBrokerRequest

Proporciona los métodos necesarios para obtener los resultados del método [**asincrónico IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

El sistema implementa esta interfaz. Se proporciona una instancia de esta interfaz al autor de la llamada con el [**método IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

## <a name="members"></a>Miembros

La **interfaz IConnectionBrokerRequest** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IConnectionBrokerRequest** tiene estos métodos.



| Método                                                      | Descripción                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Se llama para determinar el estado de una solicitud asincrónica.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest se define como 25114427-ED5D-46A6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

