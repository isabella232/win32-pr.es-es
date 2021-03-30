---
title: Interfaz IConnectionBrokerRequest (Cbclient. h)
description: Proporciona los métodos necesarios para obtener los resultados del método asincrónico IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerRequest
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerRequest, descrito
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
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803896"
---
# <a name="iconnectionbrokerrequest-interface"></a>Interfaz IConnectionBrokerRequest

Proporciona los métodos necesarios para obtener los resultados del método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) asincrónico.

El sistema implementa esta interfaz. Se proporciona una instancia de esta interfaz al llamador con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="members"></a>Miembros

La interfaz **IConnectionBrokerRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IConnectionBrokerRequest** tiene estos métodos.



| Método                                                      | Descripción                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Se llama para determinar el estado de una solicitud asincrónica.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest se define como 25114427-ED5D-46A6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

