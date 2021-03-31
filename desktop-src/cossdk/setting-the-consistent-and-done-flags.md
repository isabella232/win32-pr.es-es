---
description: Establecimiento de las marcas coherente y realizada
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Establecimiento de las marcas coherente y realizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496019"
---
# <a name="setting-the-consistent-and-done-flags"></a>Establecimiento de las marcas coherente y realizada

Puede establecer las marcas coherentes y realizadas mediante la invocación de métodos en las interfaces [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) o [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) . Las estrategias utilizadas por estas dos interfaces difieren significativamente. **IObjectContext** tiene cuatro métodos que enlazan las marcas coherente y terminada en combinaciones únicas, mientras que **IContextState** tiene dos métodos que le permiten establecer cada marca de manera independiente. Los métodos de **IObjectContext** también se exponen a través del objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Para el control independiente de cada marca, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) proporciona un método para establecer la marca coherente en true o false y un método para establecer la marca done en true o false. Estos métodos son [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) y [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn), respectivamente. La interfaz **IContextState** también incluye métodos para recuperar el valor actual de cada marca.

Al establecer el valor del método [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) en TXCOMMIT, com+ comprueba la presencia de una transacción. Si COM+ no detecta una transacción, genera un error que se puede capturar en un archivo de registro. Por ejemplo, supongamos que un usuario configura involuntariamente el atributo de transacción del componente como no compatible, pero espera que se establezca en requerido. Al establecer **SetMyTransactionVote** = TxCommit, puede identificar el conflicto y tomar medidas.

En la tabla siguiente se describen las llamadas a métodos que se pueden utilizar para establecer las marcas coherentes y finalizadas.



| Marca coherente  | Marca Done        | IObjectContext (método)                                            | IContextState (métodos)                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| True<br/>  | False<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/>  |
| False<br/> | True<br/>  | [**Tabor**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true              |



 

> [!Note]  
> La propiedad auto-Done, que se establece en el nivel de método, puede afectar al modo en que se establecen las marcas coherente y final. Para obtener más información sobre la propiedad auto-Done, consulte [habilitación de la función automática para un método](enabling-auto-done-for-a-method.md) y [establecimiento del bit Done](setting-the-done-bit.md).

 

 

 




