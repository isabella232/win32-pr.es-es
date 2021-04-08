---
description: Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Clase TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807778"
---
# <a name="transactioncontextex-class"></a>Clase TransactionContextEx

Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|--------------------------------------------------------|
| CLSID      | CLSID \_ TransactionContextEx                            |
| ProgID     | L "TxCTx. TransactionContextEx"                          |
| Interfaces | [**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Cuándo se usa

Un cliente no transaccional utiliza esta clase para iniciar una transacción. Mediante los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de la transacción del objeto de contexto de transacción. En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.

La clase **TransactionContextEx** limita la reutilización de la lógica de negocios que conduce a la transacción. Por esta razón, se recomienda que los objetos con instancias de la clase **TransactionContextEx** se utilicen con moderación.

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

La clase **TransactionContextEx** no está diseñada para utilizarse en Visual Basic. En su lugar, use la clase [**TransactionContext**](transactioncontext.md) .

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

[**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionContext**](transactioncontext.md)
</dt> </dl>

 

 




