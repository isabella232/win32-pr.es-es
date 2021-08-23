---
title: Interfaz IConnectionBrokerClient (Cbclient.h)
description: Proporciona los métodos necesarios para usar el cliente Conexión a Escritorio remoto Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Interfaz IConnectionBrokerClient Servicios de Escritorio remoto
- Interfaz IConnectionBrokerClient Servicios de Escritorio remoto , descrito
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
ms.openlocfilehash: a87c30729a5ec78e5275a6c2a1c0d9d139b857c3c7ea10f666ba09b7fceed256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059163"
---
# <a name="iconnectionbrokerclient-interface"></a>Interfaz IConnectionBrokerClient

Proporciona los métodos necesarios para usar el cliente Conexión a Escritorio remoto Broker.

El sistema implementa esta interfaz. Para obtener una instancia de esta interfaz, use la [**función CBCreateClientInstance.**](cbcreateclientinstance.md)

## <a name="members"></a>Miembros

La **interfaz IConnectionBrokerClient** hereda de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerClient también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IConnectionBrokerClient** tiene estos métodos.



| Método                                                         | Descripción                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Solicita información sobre el equipo de destino al que se debe redirigir la conexión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient se define como D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

