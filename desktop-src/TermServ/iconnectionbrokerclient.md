---
title: Interfaz IConnectionBrokerClient (Cbclient. h)
description: Proporciona los métodos necesarios para utilizar el cliente del agente de Conexión a Escritorio remoto.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerClient
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerClient, descrito
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492784"
---
# <a name="iconnectionbrokerclient-interface"></a>Interfaz IConnectionBrokerClient

Proporciona los métodos necesarios para utilizar el cliente del agente de Conexión a Escritorio remoto.

El sistema implementa esta interfaz. Para obtener una instancia de esta interfaz, utilice la función [**CBCreateClientInstance**](cbcreateclientinstance.md) .

## <a name="members"></a>Miembros

La interfaz **IConnectionBrokerClient** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerClient** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IConnectionBrokerClient** tiene estos métodos.



| Método                                                         | Descripción                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Solicita información sobre el equipo de destino al que se debe redirigir la conexión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient se define como D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

