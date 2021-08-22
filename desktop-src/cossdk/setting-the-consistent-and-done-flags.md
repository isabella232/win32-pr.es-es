---
description: Establecimiento de las marcas Coherente y Listo
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Establecimiento de las marcas Coherente y Listo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518864efda3716ea9998ed306b0ca6901b70697f8cb3acabe813d3e2e3e0bcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500055"
---
# <a name="setting-the-consistent-and-done-flags"></a>Establecimiento de las marcas Coherente y Listo

Establezca las marcas coherentes y realizadas invocando métodos en las interfaces [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) o [**IContextState.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) Las estrategias usadas por estas dos interfaces difieren significativamente. **IObjectContext tiene** cuatro métodos que enlazan las marcas coherentes y realizadas en combinaciones únicas, mientras **que IContextState** tiene dos métodos que permiten establecer cada marca de forma independiente. Los métodos **de IObjectContext también** se exponen a través del [**objeto ObjectContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)

Para un control independiente de cada marca, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) proporciona un método para establecer la marca coherente en True o False y un método para establecer la marca done en True o False. Estos métodos [**son SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) y [**SetDeactivateOnReturn,**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn)respectivamente. La **interfaz IContextState** también incluye métodos para recuperar el valor actual de cada marca.

Al establecer el valor [**del método SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) en TxCommit, COM+ comprueba la presencia de una transacción. Si COM+ no detecta una transacción, genera un error que puede capturar en un archivo de registro. Por ejemplo, suponga que alguien configura involuntariamente el atributo de transacción del componente en No admitido, pero esperaba que se estableciese en Requerido. Al establecer **SetMyTransactionVote** = TxCommit, puede identificar el conflicto y tomar medidas.

En la tabla siguiente se describen las llamadas de método que se pueden usar para establecer las marcas coherentes y realizadas.



| Marca coherente  | Marca Listo        | Método IObjectContext                                            | Métodos IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verdadero<br/>  | Falso<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/> |
| Falso<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True              |



 

> [!Note]  
> La propiedad auto-done, que se establece en el nivel de método, puede afectar a cómo se establecen las marcas coherentes y realizadas. Para obtener más información sobre la propiedad auto-done, vea Enabling Auto-Done for a Method (Habilitación de [Auto-Done para un método)](enabling-auto-done-for-a-method.md) y Setting the Done Bit (Establecer [el bit listo).](setting-the-done-bit.md)

 

 

 




