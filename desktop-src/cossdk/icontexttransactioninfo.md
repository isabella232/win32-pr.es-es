---
description: Proporciona acceso a las propiedades de objeto de contexto relacionadas con las transacciones.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: IContextTransactionInfo (interfaz)
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
ms.openlocfilehash: be470d2a06d5dc284963e76ded188cb6a11fabd963b4f1186a3cee697bdfb6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793455"
---
# <a name="icontexttransactioninfo-interface"></a>IContextTransactionInfo (interfaz)

Proporciona acceso a las propiedades de objeto de contexto relacionadas con las transacciones.

## <a name="when-to-implement"></a>Cuándo implementar

No debe implementar esta interfaz. La implementación estándar proporciona una funcionalidad completa.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz para acceder a las propiedades de objeto de contexto relacionadas con las transacciones.

## <a name="members"></a>Miembros

La **interfaz IContextTransactionInfo** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextTransactionInfo también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IContextTransactionInfo** tiene estos métodos.



| Método                                                                                         | Descripción                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Recupera la transacción o el proxy de transacción asociado al contexto actual, si existe.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de transacción raíz.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Asocia una implementación [**de ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contexto actual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/> |



 

