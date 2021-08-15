---
description: Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede componer el trabajo de varios objetos COM en una sola transacción y confirmar o anular explícitamente la transacción.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Clase TransactionContextEx (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 1293445e559e7ae1ddfda5cba10b17ee3f70082760d275a06a93c4f602cfac5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409995"
---
# <a name="transactioncontextex-class"></a>TransactionContextEx (clase)

Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede componer el trabajo de varios objetos COM en una sola transacción y confirmar o anular explícitamente la transacción.

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Valor |
|------------|--------------------------------------------------------|
| CLSID      | CLSID \_ TransactionContextEx                            |
| ProgID     | L"TxCTx.TransactionContextEx"                          |
| Interfaces | [**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Cuándo se usa

Un cliente no transaccional usa esta clase para iniciar una transacción. Con los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de transacción del objeto de contexto de transacción. En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.

La **clase TransactionContextEx limita** la reutilización de la lógica de negocios que controla la transacción. Por esta razón, se recomienda usar con moderación los objetos a los que se crea una instancia de la clase **TransactionContextEx.**

## <a name="remarks"></a>Comentarios

Para crear este objeto, llame a [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

La **clase TransactionContextEx** no se diseñó para usarse en Visual Basic. Use la [**clase TransactionContext**](transactioncontext.md) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Configuración de transacciones](configuring-transactions.md)
</dt> <dt>

[**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionContext**](transactioncontext.md)
</dt> </dl>

 

 




