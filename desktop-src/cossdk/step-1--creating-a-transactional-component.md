---
description: 'Paso 1: crear un componente transaccional'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Paso 1: crear un componente transaccional'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104361785"
---
# <a name="step-1-creating-a-transactional-component"></a>Paso 1: crear un componente transaccional

## <a name="objectives"></a>Objetivos

En este paso, aprenderá lo siguiente:

-   Cómo escribir un componente transaccional en Microsoft Visual Basic
-   ¿Cuál es la configuración predeterminada para los servicios COM+?
-   Cómo configurar servicios COM+

## <a name="description"></a>Descripción

El componente UpdateAuthorAddress, que se crea en esta sección, actualiza la dirección de un autor existente en la base de datos pubs. La base de datos pubs es una base de datos de ejemplo que se incluye con Microsoft SQL Server. Contiene información de publicación, como nombres de autor, direcciones y títulos de libros.

> [!Note]  
> Pubs es el almacén de datos que se usa en este manual.

 

Dado que UpdateAuthorAddress actualiza un almacén de datos, es aconsejable incluir el trabajo en una transacción, como se muestra en la siguiente ilustración, de modo que cuando un cliente llama al componente, COM+ inicia automáticamente una transacción y da de alta la base de datos (Resource Manager) en esa transacción. (Para obtener información detallada acerca de las transacciones en COM+, consulte [transacciones com+](com--transactions.md)).

![Diagrama que muestra una transacción de COM+ con UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Para convertir UpdateAuthorAddress en un componente transaccional, se requieren los siguientes pasos:

1.  Debe escribirse el componente. Para obtener protección adicional, se agrega una subrutina, comprobando que COM+ creó el objeto en una transacción. Además, el control de errores básico se incluye en el componente para simplificar la recuperación de errores. La comprobación de transacciones y el control de errores mejoran la confiabilidad del componente. (Consulte el código de ejemplo del paso 1 para obtener una lista completa del componente UpdateAuthorAddress).
2.  Después de agregar el componente a una aplicación COM+ e instalar la aplicación, el atributo Transaction debe establecerse en **required**, lo que garantiza que com+ crea cada objeto UpdateAuthorAddress en una transacción. Para obtener instrucciones sobre cómo establecer el atributo de transacción para un componente, vea [establecer el atributo de transacción](setting-the-transaction-attribute.md).
    > [!Note]  
    > Al establecer el atributo de transacción en un componente, se define cómo crea COM+ cada objeto con respecto a las transacciones. Los valores de atributo de transacción se **omiten**, **no se admiten**, se **admiten**, son **obligatorios** y **requieren New**. El valor **requerido** no es ninguno de los valores de atributo predeterminados de un componente.

     

COM+ enlaza el servicio de transacciones con la activación Just-in-Time (JIT) y la simultaneidad. Al declarar un componente como transaccional, COM+ también aplica la activación JIT y la protección de simultaneidad (sincronización).

## <a name="sample-code"></a>Código de ejemplo

El componente UpdateAuthorAddress abre una conexión a la base de datos pubs, lo que permite al usuario modificar el nombre, la dirección o el estado del contrato del autor. También llama a un segundo componente, que se describe en [paso 2: extensión de una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md).

Para usar el siguiente código en un proyecto de Microsoft Visual Basic, abra un nuevo proyecto de ActiveX.dll y agregue referencias a la biblioteca de Microsoft Objetos de datos ActiveX y a la biblioteca de tipos de servicios COM+.

> [!Note]  
> El código de ejemplo de este manual es para fines ilustrativos y puede que no sea el más eficaz para el almacenamiento provisional real y la producción.

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a>Resumen

-   COM+ asigna los valores de atributo predeterminados. Puede volver a configurar la mayoría de los atributos de servicio.
-   Establecer el atributo de transacción de un componente en **required** garantiza que com+ debe crear cada instancia de ese componente en una transacción, pero no inicia necesariamente una nueva transacción.
-   Comprobar la presencia de una transacción confirma que el valor del atributo de transacción del componente no se ha restablecido involuntariamente a un valor no transaccional, como **omitir** o **no se admite**.
-   El control de errores hace que el componente sea más confiable y más fácil de solucionar.
-   COM+ aplica los servicios de protección de [simultaneidad](com--synchronization.md) y [activación JIT](com--just-in-time-activation.md) para los componentes transaccionales.
-   Al cerrar la conexión de la base de datos cuando haya terminado, se permite que otro componente de la misma transacción reutilice la conexión del grupo de conexiones. (La agrupación de conexiones no se debe confundir con la [agrupación de objetos](com--object-pooling.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Paso 2: extensión de una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Paso 3: reutilización de componentes](step-3--reusing-components.md)
</dt> <dt>

[Activación Just-in-Time de COM+](com--just-in-time-activation.md)
</dt> <dt>

[Sincronización de COM+](com--synchronization.md)
</dt> <dt>

[Configuración de transacciones](configuring-transactions.md)
</dt> <dt>

[Crear aplicaciones COM+](creating-com--applications.md)
</dt> <dt>

[Establecer el atributo de transacción](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



