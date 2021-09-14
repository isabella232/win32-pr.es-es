---
description: 'Paso 2: Extender una transacción entre varios componentes'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Paso 2: Extender una transacción entre varios componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361644"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Paso 2: Extender una transacción entre componentes

## <a name="objectives"></a>Objetivos

En este paso, aprenderá lo siguiente:

-   Flujo de transacción
-   Cómo votan varios objetos en una transacción

## <a name="description"></a>Descripción

[Paso 1: Crear un](step-1--creating-a-transactional-component.md) componente transaccional muestra cómo escribir un componente transaccional simple que actualiza la información del autor en la base de datos Microsoft SQL Server de Pubs. En el paso 2 se muestra lo que sucede cuando una transacción se extiende entre varios componentes.

De acuerdo con el modelo de programación de COM+, llama a otro componente en `UpdateAuthorAddress` el transcurso de completar su trabajo. El segundo componente, , valida la dirección del autor y `ValidateAuthorAddress` devuelve los resultados a su autor de la llamada, `UpdateAuthorAddress` .

A diferencia de su `ValidateAuthorAddress` autor de la llamada, no requiere una transacción, pero todavía puede participar en la transacción de su autor de la llamada. En este paso, su valor de atributo de transacción se establece en **Compatible,** como se muestra en la ilustración siguiente, que extiende la transacción existente al nuevo objeto.

![Diagrama que muestra la extensión de la transacción existente al nuevo objeto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

El **valor de** atributo Compatible extiende (o fluye) una transacción existente solo cuando el autor de la llamada es transaccional. Cuando llama a , COM+ examina primero el contexto del autor de `UpdateAuthorAddress` la llamada para ver si es `ValidateAuthorAddress` transaccional. A continuación, COM+ examina los atributos de servicio que están establecidos en y asigna al nuevo objeto el mismo identificador de transacción `ValidateAuthorAddress` asignado al objeto llamador. Para comprender mejor este proceso, vea [Activación de contexto.](context-activation.md)

Dado que comparten el mismo identificador de transacción, ambos objetos deben completar su trabajo correctamente o COM+ anula la transacción (deshaciendo los cambios realizados en la base de datos de Pubs).

Todos los objetos que participan en una transacción votan para confirmar o anular la transacción. La votación se produce explícitamente cuando se incluyen instrucciones de votación en el código, como se muestra en la siguiente extracción del código de ejemplo del paso 1, que crea el `UpdateAuthorAddress` componente:


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



La votación también se produce implícitamente, como se hace en el `ValidateAuthorAddress` componente . A menos que el objeto declare lo contrario, COM+ supone que un objeto ha completado su trabajo correctamente, pero que no está listo para desactivarse. COM+ realiza la siguiente suposición:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Cuando `ValidateAuthorAddress` vuelve a su autor de la llamada, COM+ lee su voto como una confirmación. COM+ no cuenta los votos hasta que desactiva el objeto raíz, que es el primer objeto de la transacción en este caso, el `UpdateAuthorAddress` objeto .

## <a name="sample-code"></a>Código de ejemplo

El `ValidateAuthorAddress` componente realiza una comprobación simple de la dirección del autor. Dado `UpdateAuthorAddress` que no vota explícitamente, COM+ usa la configuración de voto predeterminada.


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

-   Establecer el atributo de transacción de un componente en **Compatible** puede dar lugar a que el nuevo objeto se cree en la transacción del objeto que realiza la llamada. COM+ examina el contexto del autor de la llamada para determinar el estado transaccional del nuevo objeto. Si el autor de la llamada es transaccional, COM+ fluye la transacción al nuevo objeto .
-   Todos los objetos que participan en la misma transacción comparten un identificador de transacción común, que COM+ lee del contexto del objeto.
-   Cada objeto de una transacción vota independientemente de otros objetos. COM+ cuenta los votos cuando se desactiva el objeto raíz.
-   Puede alternar el voto de transacción de un objeto entre confirmar y anular hasta que COM+ desactive el objeto o hasta que COM+ desactive el objeto raíz y finalice la transacción. Solo cuenta la configuración del último voto. Las [**interfaces IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) [**e IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) proporcionan métodos y que generan resultados de votación similares, como se muestra en la tabla siguiente. Puede usar cualquiera de las interfaces para votar explícitamente en una transacción. 

    | [**Métodos de combinación IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | [**Método equivalente de IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ establece el voto de un objeto en el equivalente de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) a menos que el componente vote explícitamente.
-   Votar explícitamente puede reducir la duración total de la transacción y liberar bloqueos de recursos costosos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Paso 1: Crear un componente transaccional](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Paso 3: Reusar componentes](step-3--reusing-components.md)
</dt> <dt>

[Activación de contexto](context-activation.md)
</dt> <dt>

[Administración de transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




