---
description: 'Paso 2: extensión de una transacción en varios componentes'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Paso 2: extensión de una transacción en varios componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104361786"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Paso 2: extensión de una transacción entre componentes

## <a name="objectives"></a>Objetivos

En este paso, obtendrá información sobre lo siguiente:

-   Flujo de transacción
-   Cómo votan varios objetos en una transacción

## <a name="description"></a>Descripción

[Paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md) muestra cómo escribir un componente transaccional simple que actualiza la información de autor en la base de datos de Microsoft SQL Server pubs. En el paso 2 se muestra lo que sucede cuando una transacción se extiende por varios componentes.

En consonancia con el modelo de programación COM+, `UpdateAuthorAddress` llama a otro componente en el transcurso de la finalización de su trabajo. El segundo componente, `ValidateAuthorAddress` , valida la dirección del autor y devuelve los resultados a su llamador, `UpdateAuthorAddress` .

A diferencia de su llamador, no `ValidateAuthorAddress` requiere una transacción, pero todavía puede participar en la transacción del llamador. En este paso, su valor de atributo de transacción se establece en **compatible**, tal como se muestra en la siguiente ilustración, que extiende la transacción existente al nuevo objeto.

![Diagrama que muestra la extensión de la transacción existente al nuevo objeto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

El valor de atributo **compatible** extiende (o fluye) una transacción existente solo cuando el autor de la llamada es transaccional. Cuando `UpdateAuthorAddress` llama a `ValidateAuthorAddress` , com+ busca primero en el contexto del autor de la llamada para ver si es transaccional. Después, COM+ examina los atributos de servicio que están establecidos en `ValidateAuthorAddress` y asigna al nuevo objeto el mismo identificador de transacción que se asigna al objeto de llamador. Para comprender mejor este proceso, consulte [activación de contexto](context-activation.md).

Dado que comparten el mismo identificador de transacción, ambos objetos deben completar su trabajo correctamente o COM+ anula la transacción (deshaciendo los cambios realizados en la base de datos pubs).

Todos los objetos que participan en una transacción votan para confirmar o anular la transacción. La votación se produce explícitamente cuando se incluyen instrucciones de votación en el código, tal y como se muestra en la siguiente extracción del código de ejemplo del paso 1, que crea el `UpdateAuthorAddress` componente:


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



La votación también se produce implícitamente, como se hace en el `ValidateAuthorAddress` componente. A menos que el objeto declare lo contrario, COM+ supone que un objeto ha completado su trabajo correctamente, pero que no está listo para desactivarse. COM+ hace lo siguiente:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Cuando `ValidateAuthorAddress` vuelve a su llamador, com+ lee su votación como confirmación. COM+ no cuenta los votos hasta que desactiva el objeto raíz, que es el primer objeto de la transacción en este caso, el `UpdateAuthorAddress` objeto.

## <a name="sample-code"></a>Código de ejemplo

El `ValidateAuthorAddress` componente realiza una comprobación simple de la dirección del autor. Dado `UpdateAuthorAddress` que no vota explícitamente, com+ usa la configuración de votación predeterminada.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a>Resumen

-   Establecer el atributo de transacción de un componente en **compatible** puede dar lugar a que se cree el nuevo objeto en la transacción del objeto que realiza la llamada. COM+ examina el contexto del llamador para determinar el estado transaccional del nuevo objeto. Si el autor de la llamada es transaccional, COM+ transfiere la transacción al nuevo objeto.
-   Todos los objetos que participan en la misma transacción comparten un identificador de transacción común, que COM+ lee en el contexto del objeto.
-   Cada objeto de una transacción vota independientemente de otros objetos. COM+ cuenta los votos cuando se desactiva el objeto raíz.
-   Puede alternar el voto de transacciones de un objeto entre commit y Abort hasta que COM+ desactive el objeto o hasta que COM+ desactive el objeto raíz y finalice la transacción. Solo el último valor de votación es Count. Las interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) y [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) proporcionan métodos y que generan resultados de votación similares, tal como se muestra en la tabla siguiente. Puede utilizar cualquiera de las interfaces para votar explícitamente en una transacción. 

    | Métodos de combinación de [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | Método equivalente de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>   | [**Tabor**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ establece el voto de un objeto en el equivalente de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) a menos que el componente vote explícitamente.
-   La votación explícitamente puede reducir la duración total de la transacción y liberar bloqueos de recursos costosos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Paso 3: reutilización de componentes](step-3--reusing-components.md)
</dt> <dt>

[Activación de contexto](context-activation.md)
</dt> <dt>

[Administrar transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




