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
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="3846e-103">Paso 1: crear un componente transaccional</span><span class="sxs-lookup"><span data-stu-id="3846e-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="3846e-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="3846e-104">Objectives</span></span>

<span data-ttu-id="3846e-105">En este paso, aprenderá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3846e-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="3846e-106">Cómo escribir un componente transaccional en Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3846e-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="3846e-107">¿Cuál es la configuración predeterminada para los servicios COM+?</span><span class="sxs-lookup"><span data-stu-id="3846e-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="3846e-108">Cómo configurar servicios COM+</span><span class="sxs-lookup"><span data-stu-id="3846e-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="3846e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3846e-109">Description</span></span>

<span data-ttu-id="3846e-110">El componente UpdateAuthorAddress, que se crea en esta sección, actualiza la dirección de un autor existente en la base de datos pubs.</span><span class="sxs-lookup"><span data-stu-id="3846e-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="3846e-111">La base de datos pubs es una base de datos de ejemplo que se incluye con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3846e-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="3846e-112">Contiene información de publicación, como nombres de autor, direcciones y títulos de libros.</span><span class="sxs-lookup"><span data-stu-id="3846e-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="3846e-113">Pubs es el almacén de datos que se usa en este manual.</span><span class="sxs-lookup"><span data-stu-id="3846e-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="3846e-114">Dado que UpdateAuthorAddress actualiza un almacén de datos, es aconsejable incluir el trabajo en una transacción, como se muestra en la siguiente ilustración, de modo que cuando un cliente llama al componente, COM+ inicia automáticamente una transacción y da de alta la base de datos (Resource Manager) en esa transacción.</span><span class="sxs-lookup"><span data-stu-id="3846e-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="3846e-115">(Para obtener información detallada acerca de las transacciones en COM+, consulte [transacciones com+](com--transactions.md)).</span><span class="sxs-lookup"><span data-stu-id="3846e-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Diagrama que muestra una transacción de COM+ con UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="3846e-117">Para convertir UpdateAuthorAddress en un componente transaccional, se requieren los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="3846e-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="3846e-118">Debe escribirse el componente.</span><span class="sxs-lookup"><span data-stu-id="3846e-118">The component must be written.</span></span> <span data-ttu-id="3846e-119">Para obtener protección adicional, se agrega una subrutina, comprobando que COM+ creó el objeto en una transacción.</span><span class="sxs-lookup"><span data-stu-id="3846e-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="3846e-120">Además, el control de errores básico se incluye en el componente para simplificar la recuperación de errores.</span><span class="sxs-lookup"><span data-stu-id="3846e-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="3846e-121">La comprobación de transacciones y el control de errores mejoran la confiabilidad del componente.</span><span class="sxs-lookup"><span data-stu-id="3846e-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="3846e-122">(Consulte el código de ejemplo del paso 1 para obtener una lista completa del componente UpdateAuthorAddress).</span><span class="sxs-lookup"><span data-stu-id="3846e-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="3846e-123">Después de agregar el componente a una aplicación COM+ e instalar la aplicación, el atributo Transaction debe establecerse en **required**, lo que garantiza que com+ crea cada objeto UpdateAuthorAddress en una transacción.</span><span class="sxs-lookup"><span data-stu-id="3846e-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="3846e-124">Para obtener instrucciones sobre cómo establecer el atributo de transacción para un componente, vea [establecer el atributo de transacción](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="3846e-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="3846e-125">Al establecer el atributo de transacción en un componente, se define cómo crea COM+ cada objeto con respecto a las transacciones.</span><span class="sxs-lookup"><span data-stu-id="3846e-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="3846e-126">Los valores de atributo de transacción se **omiten**, **no se admiten**, se **admiten**, son **obligatorios** y **requieren New**.</span><span class="sxs-lookup"><span data-stu-id="3846e-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="3846e-127">El valor **requerido** no es ninguno de los valores de atributo predeterminados de un componente.</span><span class="sxs-lookup"><span data-stu-id="3846e-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="3846e-128">COM+ enlaza el servicio de transacciones con la activación Just-in-Time (JIT) y la simultaneidad.</span><span class="sxs-lookup"><span data-stu-id="3846e-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="3846e-129">Al declarar un componente como transaccional, COM+ también aplica la activación JIT y la protección de simultaneidad (sincronización).</span><span class="sxs-lookup"><span data-stu-id="3846e-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="3846e-130">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3846e-130">Sample code</span></span>

<span data-ttu-id="3846e-131">El componente UpdateAuthorAddress abre una conexión a la base de datos pubs, lo que permite al usuario modificar el nombre, la dirección o el estado del contrato del autor.</span><span class="sxs-lookup"><span data-stu-id="3846e-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="3846e-132">También llama a un segundo componente, que se describe en [paso 2: extensión de una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md).</span><span class="sxs-lookup"><span data-stu-id="3846e-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="3846e-133">Para usar el siguiente código en un proyecto de Microsoft Visual Basic, abra un nuevo proyecto de ActiveX.dll y agregue referencias a la biblioteca de Microsoft Objetos de datos ActiveX y a la biblioteca de tipos de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="3846e-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="3846e-134">El código de ejemplo de este manual es para fines ilustrativos y puede que no sea el más eficaz para el almacenamiento provisional real y la producción.</span><span class="sxs-lookup"><span data-stu-id="3846e-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


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



## <a name="summary"></a><span data-ttu-id="3846e-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="3846e-135">Summary</span></span>

-   <span data-ttu-id="3846e-136">COM+ asigna los valores de atributo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3846e-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="3846e-137">Puede volver a configurar la mayoría de los atributos de servicio.</span><span class="sxs-lookup"><span data-stu-id="3846e-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="3846e-138">Establecer el atributo de transacción de un componente en **required** garantiza que com+ debe crear cada instancia de ese componente en una transacción, pero no inicia necesariamente una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="3846e-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="3846e-139">Comprobar la presencia de una transacción confirma que el valor del atributo de transacción del componente no se ha restablecido involuntariamente a un valor no transaccional, como **omitir** o **no se admite**.</span><span class="sxs-lookup"><span data-stu-id="3846e-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="3846e-140">El control de errores hace que el componente sea más confiable y más fácil de solucionar.</span><span class="sxs-lookup"><span data-stu-id="3846e-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="3846e-141">COM+ aplica los servicios de protección de [simultaneidad](com--synchronization.md) y [activación JIT](com--just-in-time-activation.md) para los componentes transaccionales.</span><span class="sxs-lookup"><span data-stu-id="3846e-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="3846e-142">Al cerrar la conexión de la base de datos cuando haya terminado, se permite que otro componente de la misma transacción reutilice la conexión del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="3846e-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="3846e-143">(La agrupación de conexiones no se debe confundir con la [agrupación de objetos](com--object-pooling.md)).</span><span class="sxs-lookup"><span data-stu-id="3846e-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3846e-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3846e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3846e-145">Paso 2: extensión de una transacción en varios componentes</span><span class="sxs-lookup"><span data-stu-id="3846e-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="3846e-146">Paso 3: reutilización de componentes</span><span class="sxs-lookup"><span data-stu-id="3846e-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="3846e-147">Activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="3846e-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="3846e-148">Sincronización de COM+</span><span class="sxs-lookup"><span data-stu-id="3846e-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="3846e-149">Configuración de transacciones</span><span class="sxs-lookup"><span data-stu-id="3846e-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="3846e-150">Crear aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="3846e-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="3846e-151">Establecer el atributo de transacción</span><span class="sxs-lookup"><span data-stu-id="3846e-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



