---
description: Crea un objeto transaccional genérico que comienza una transacción.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Clase TransactionContext (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: aa0a90cee2b0af7d5ebe3679dca46aa04c6326fb5fd62fe5f57699d610b9efe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678155"
---
# <a name="transactioncontext-class"></a>Clase TransactionContext

Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede componer el trabajo de varios objetos COM en una sola transacción y confirmar o anular explícitamente la transacción.

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Value |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionContext                          |
| ProgID     | L"TxCTx.TransactionContext"                        |
| Interfaces | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Cuándo se usa

Un cliente no transaccional usa esta clase para iniciar una transacción. Con los métodos de esta clase, el cliente puede llamar a objetos COM adicionales que, si están configurados para participar en una transacción, se ejecutan dentro del límite de transacción del objeto de contexto de transacción. En función de su lógica de negocios, el cliente puede confirmar o anular explícitamente la transacción.

La **clase TransactionContext** limita la reutilización de la lógica de negocios que controla la transacción. Por esta razón, se recomienda usar con moderación los objetos a los que se crea una instancia de la clase **TransactionContext.**

## <a name="remarks"></a>Comentarios

Para crear este objeto, llame a [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto TransactionContext se puede declarar mediante "COMSVCSLib.TransactionContext" como nombre de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Configuración de transacciones](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




