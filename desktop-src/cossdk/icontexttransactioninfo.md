---
description: Proporciona acceso a las propiedades del objeto de contexto relacionadas con las transacciones.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interfaz IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496331"
---
# <a name="icontexttransactioninfo-interface"></a>Interfaz IContextTransactionInfo

Proporciona acceso a las propiedades del objeto de contexto relacionadas con las transacciones.

## <a name="when-to-implement"></a>Cuándo implementar

No debe implementar esta interfaz. La implementación estándar proporciona una funcionalidad completa.

## <a name="when-to-use"></a>Cuándo se usa

Utilice esta interfaz para tener acceso a las propiedades del objeto de contexto relacionadas con las transacciones.

## <a name="members"></a>Miembros

La interfaz **IContextTransactionInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextTransactionInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IContextTransactionInfo** tiene estos métodos.



| Método                                                                                         | Descripción                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Asocia una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) con el contexto actual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/> |



 

