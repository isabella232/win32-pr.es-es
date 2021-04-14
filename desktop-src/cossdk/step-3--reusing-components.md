---
description: 'Paso 3: reutilización de componentes'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Paso 3: reutilización de componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104555615"
---
# <a name="step-3-reusing-components"></a>Paso 3: reutilización de componentes

## <a name="objectives"></a>Objetivos

En este paso, obtendrá información sobre lo siguiente:

-   Componentes reutilizables.
-   Cómo planear la reutilización.

## <a name="description"></a>Descripción

Dos partes anteriores de este manual de servicios COM+, [paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md) y [paso 2: extender una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md) mostrar cómo escribir un componente que llame a un segundo componente para ayudar a completar algún trabajo, actualizar la información de autor en la base de datos de Microsoft SQL Server pubs; todo el trabajo está protegido por una sola transacción. Los componentes de ejemplo se centran en el trabajo de actualización de los datos de un autor y en la comprobación de la dirección del autor, y en el procesamiento de transacciones proporcionado por COM+, la [activación JIT](com--just-in-time-activation.md)y la [protección de simultaneidad](com--synchronization.md).

En este paso se muestra cómo reutilizar los componentes creados en los pasos 1 y 2 y se examina lo que esto significa para el diseño de esos componentes. Como se muestra en la siguiente ilustración, esto significa que se crea un nuevo componente, `AddNewAuthor` , que agrega nuevos autores a la base de datos mediante una llamada a `UpdateAuthorAddress` .

![Diagrama que muestra el flujo cuando se reutilizan los componentes.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Además de reutilizar la funcionalidad de componentes existente, `AddNewAuthor` llama a otro nuevo componente denominado `ValidateAuthorName` . Como muestra la ilustración anterior, `ValidateAuthorName` es no transaccional. El valor del atributo de transacción para este componente se deja en su configuración predeterminada (**no se admite**) para excluir su trabajo de la transacción. Como se muestra en el código de ejemplo del paso 3, `ValidateAuthorName` realiza consultas de solo lectura en la base de datos y el error de esta tarea secundaria no debe tener la posibilidad de anular la transacción. Sin embargo, el valor de atributo de transacción del `AddNewAuthor` componente se establece en **required**.

`AddNewAuthor`Todos los componentes de, `UpdateAuthorAddress` y `ValidateAuthorAddress` votan en la transacción. En esta transacción, `AddNewAuthor` es el objeto raíz. COM+ siempre hace que el primer objeto creado en la transacción sea el objeto raíz.

En este ejemplo, la reutilización del `UpdateAuthorAddress` componente es fácil: com + proporciona automáticamente los servicios esperados. Sin embargo, los resultados serían diferentes si el valor del atributo de transacción del `UpdateAuthorAddress` componente se hubiera establecido inicialmente en **requiere New** en lugar de **required**. En la superficie, ambos valores aparecen de forma similar. ambos garantizan una transacción. **Requiere New**, sin embargo, siempre inicia una nueva transacción, mientras que **required** inicia una nueva transacción solo cuando el autor de la llamada del objeto es no transaccional. Puede ver, en este aspecto, lo importante que conviene configurar con `UpdateAuthorAddress` cuidado y de forma minuciosa. De lo contrario, COM+ podría haber interpretado la solicitud de servicio de forma diferente, generando dos transacciones no relacionadas, tal como se muestra en la siguiente ilustración, en lugar de una.

![Diagrama que muestra el flujo al reutilizar los componentes con "requires New".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Cuando vuelva a usar los componentes, asegúrese de que los servicios estén configurados para admitir el resultado deseado.

 

## <a name="sample-code"></a>Código de ejemplo

El componente AddNewAuthor realiza agregaciones por lotes de nuevos autores permitiendo que el objeto permanezca activo hasta que el cliente libere su referencia al objeto.


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



El `ValidateAuthorName` componente valida los nombres de autor antes de `AddNewAuthor` Agregar el nombre a la base de datos. Este componente produce un error en el autor de la llamada si se produce algo inesperado.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a>Resumen

-   Hay ocasiones en las que no desea que un componente vote en la transacción.
-   COM+ no aplica la activación JIT ni la protección de simultaneidad en componentes no transaccionales. Puede configurar estos servicios por separado.
-   La configuración de un componente que realiza la llamada afecta a cómo COM+ interpreta las solicitudes de servicio del componente al que se ha llamado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Paso 2: extensión de una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Configuración de transacciones](configuring-transactions.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> </dl>

 

 



