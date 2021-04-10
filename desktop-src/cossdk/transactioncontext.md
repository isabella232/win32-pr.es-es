---
description: Crea un objeto transaccional genérico que comienza una transacción.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Clase TransactionContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275066"
---
# <a name="transactioncontext-class"></a>Clase TransactionContext

Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionContext                          |
| ProgID     | L "TxCTx. TransactionContext"                        |
| Interfaces | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Cuándo se usa

Un cliente no transaccional utiliza esta clase para iniciar una transacción. Mediante los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de la transacción del objeto de contexto de transacción. En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.

La clase **TransactionContext** limita la reutilización de la lógica de negocios que conduce a la transacción. Por esta razón, se recomienda que los objetos con instancias de la clase **TransactionContext** se utilicen con moderación.

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto TransactionContext se puede declarar con "COMSVCSLib. TransactionContext" como nombre de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Configuración de transacciones](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




