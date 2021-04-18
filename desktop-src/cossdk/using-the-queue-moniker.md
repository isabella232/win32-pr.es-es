---
description: El moniker de cola se utiliza para activar un componente en cola mediante programación.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Usar el moniker de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705316"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="d5c7b-103">Usar el moniker de cola</span><span class="sxs-lookup"><span data-stu-id="d5c7b-103">Using the Queue Moniker</span></span>

<span data-ttu-id="d5c7b-104">El moniker de cola se utiliza para activar un componente en cola mediante programación.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="d5c7b-105">El moniker de cola requiere que reciba el ID. de clase (CLSID) del objeto que se va a invocar desde el nuevo moniker directamente a la derecha.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="d5c7b-106">Cuando se prefijan a la izquierda, el nuevo moniker pasa el CLSID al moniker a su izquierda.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="d5c7b-107">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="d5c7b-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="d5c7b-108">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d5c7b-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d5c7b-109">Visual Basic</span></span>

<span data-ttu-id="d5c7b-110">El parámetro de nombre para mostrar de GetObject es "Queue:/New:", seguido del identificador de programa o el GUID de formulario de cadena, con o sin llaves, del objeto de servidor del que se va a crear una instancia.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="d5c7b-111">En los siguientes ejemplos se muestran tres activaciones válidas de un componente con el moniker de cola:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="d5c7b-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="d5c7b-112">C/C++</span></span>

<span data-ttu-id="d5c7b-113">El parámetro de nombre para mostrar de [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) es "Queue:/New:", seguido del identificador de programa o el GUID de formulario de cadena, con o sin llaves, del objeto de servidor del que se va a crear una instancia.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="d5c7b-114">En los siguientes ejemplos se muestran tres activaciones válidas de un componente con el moniker de cola:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="d5c7b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c7b-115">Remarks</span></span>

<span data-ttu-id="d5c7b-116">El moniker de cola acepta parámetros opcionales que modifican las propiedades del mensaje enviado a Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="d5c7b-117">Por ejemplo, para que el mensaje de Message Queuing se envíe con prioridad 6, el componente en cola se activaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="d5c7b-118">En la tabla siguiente se enumeran los parámetros de moniker de cola que afectan a la cola de destino.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5c7b-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d5c7b-119">Parameter</span></span></th>
<th><span data-ttu-id="d5c7b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5c7b-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5c7b-121"><em>nombreDeEquipo</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-122">Especifica la parte del nombre de equipo de un nombre de ruta de acceso de cola de Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="d5c7b-123">El nombre de la ruta de acceso de la cola de Message Queue Server tiene el formato <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="d5c7b-124">Si no se especifica, se utiliza el nombre de equipo asociado a la aplicación configurada.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-126">Especifica el nombre de la cola de Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="d5c7b-127">El nombre de la ruta de acceso de la cola de Message Queue Server tiene el formato <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="d5c7b-128">Si no se especifica, se utiliza el nombre de cola asociado a la aplicación configurada.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="d5c7b-129">Para obtener una cola no transaccional, puede especificar primero el nombre de la cola y, a continuación, crear una aplicación COM+ con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-131">Especifica el nombre completo de la ruta de la cola de Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="d5c7b-132">Si no se especifica, se utiliza el nombre de la ruta de acceso de la cola de Message Queue Server asociada a la aplicación configurada.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="d5c7b-133">Para invalidar el nombre de destino, la ruta de acceso se puede especificar en el formato siguiente para la instalación de un grupo de trabajo de Message Queue Server:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="d5c7b-134">Queue:<em>nombreruta</em> = <em>ComputerName</em>\PRIVATE $ \ appname/New: mi proyecto. CMyClass</span><span class="sxs-lookup"><span data-stu-id="d5c7b-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d5c7b-135">Tanto el lenguaje de programación C como el Microsoft Visual C++ requieren dos barras diagonales inversas para representar una barra diagonal inversa dentro de literales de cadena, por ejemplo, nómina de Chicago \\ .</span><span class="sxs-lookup"><span data-stu-id="d5c7b-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-136"><em>FormatName</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-137">Al marcar una aplicación COM+ como en cola, COM+ crea una cola de Message Queue Server cuyo nombre es el mismo que el de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="d5c7b-138">El nombre de formato de Message Queue Server de esa cola está en el catálogo de COM+, asociado a la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="d5c7b-139">Para reemplazar el nombre de destino, el nombre de formato se puede especificar en el formato siguiente para una instalación de grupo de trabajo de Message Queue Server:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="d5c7b-140">Queue:<em>FormatName</em>= Direct = os:<em>ComputerName</em>\PRIVATE $ \ appname/New: ProgID</span><span class="sxs-lookup"><span data-stu-id="d5c7b-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="d5c7b-141">En una configuración de Active Directory, &quot; &quot; no se especifica Private $ como parte del nombre de la cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="d5c7b-142">Los parámetros opcionales de moniker de cola se procesan de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="d5c7b-143">Especifique cada palabra clave solo una vez.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-143">Specify each keyword only one time.</span></span> <span data-ttu-id="d5c7b-144">Al especificar el parámetro *PathName* , se reemplazan los parámetros *ComputerName* y *QueueName*.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="d5c7b-145">Un parámetro *FormatName* específico elimina el conocimiento anterior de un parámetro *ComputerName*, *QueueName* y *PathName* .</span><span class="sxs-lookup"><span data-stu-id="d5c7b-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="d5c7b-146">Asociar el agente de escucha de componentes en cola con una cola privada específica</span><span class="sxs-lookup"><span data-stu-id="d5c7b-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="d5c7b-147">El agente de escucha de componentes en cola de COM+ recibe solo de las colas asociadas a la aplicación COM+ marcada como en cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="d5c7b-148">Al marcar una aplicación COM+ como en cola, COM+ crea una cola de Message Queue Server cuyo nombre es el mismo que el de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="d5c7b-149">El nombre de formato de Message Queue Server de esa cola está en el catálogo de COM+, asociado a la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="d5c7b-150">Cuando se inicia la aplicación COM+ y se marca como de escucha, se inicia un agente de escucha en el proceso de la aplicación COM+ y se abre la cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="d5c7b-151">En la tabla siguiente se enumeran los parámetros de moniker de cola que afectan al mensaje de Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5c7b-152">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d5c7b-152">Parameter</span></span></th>
<th><span data-ttu-id="d5c7b-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5c7b-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5c7b-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-155">Especifica un entero sin signo, por ejemplo, AppSpecific = 12345.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-157">Especifica el nivel de autenticación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-157">Specifies the message authentication level.</span></span> <span data-ttu-id="d5c7b-158">Un mensaje autenticado está firmado digitalmente y requiere un certificado para el usuario que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="d5c7b-159">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="d5c7b-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="d5c7b-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-162"><em>Entrega.</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-163">Especifica la opción de entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-163">Specifies the message delivery option.</span></span> <span data-ttu-id="d5c7b-164">Este valor se omite para las colas transaccionales.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="d5c7b-165">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="d5c7b-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="d5c7b-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-168"><em>EncryptAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-169">Especifica el algoritmo de cifrado que va a usar Message Queue Server para cifrar y descifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="d5c7b-170">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-171">CALG_RC2, CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="d5c7b-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="d5c7b-172">Cualquier valor entero que sea aceptable para Message Queue Server para un <em>EncryptAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-174">Especifica una función hash criptográfica.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="d5c7b-175">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="d5c7b-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="d5c7b-177">Cualquier valor entero que sea aceptable para Message Queue para un <em>HashAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-178">Diario</span><span class="sxs-lookup"><span data-stu-id="d5c7b-178">Journal</span></span><br/></td>
<td><span data-ttu-id="d5c7b-179">Especifica la opción del diario de mensajes de Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="d5c7b-180">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="d5c7b-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="d5c7b-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="d5c7b-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="d5c7b-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-184"><em>Label</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-185">Especifica una cadena de etiqueta de mensaje hasta MQ_MAX_MSG_LABEL_LEN caracteres.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-186"><em>MaxTimeToReachQueue</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-187">Especifica el tiempo máximo, en segundos, para que el mensaje llegue a la cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="d5c7b-188">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="d5c7b-189">INFINITE</span></span></li>
<li><span data-ttu-id="d5c7b-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="d5c7b-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="d5c7b-191">Número de segundos</span><span class="sxs-lookup"><span data-stu-id="d5c7b-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-192"><em>MaxTimeToReceive</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-193">Especifica el tiempo máximo, en segundos, para que la aplicación de destino reciba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="d5c7b-194">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="d5c7b-195">INFINITE</span></span></li>
<li><span data-ttu-id="d5c7b-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="d5c7b-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="d5c7b-197">Número de segundos</span><span class="sxs-lookup"><span data-stu-id="d5c7b-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-198"><em>Prioridad</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-199">Especifica un nivel de prioridad de mensaje, dentro de los valores de Message Queue Server permitidos.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="d5c7b-200">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="d5c7b-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="d5c7b-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="d5c7b-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="d5c7b-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="d5c7b-204">Número entre 0 y 7</span><span class="sxs-lookup"><span data-stu-id="d5c7b-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5c7b-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-206">Especifica un nivel de privacidad, que se usa para cifrar mensajes.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="d5c7b-207">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-208">MQMSG_PRIV_LEVEL_NONE, NINGUNO, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="d5c7b-209">MQMSG_PRIV_LEVEL_BODY, CUERPO,</span><span class="sxs-lookup"><span data-stu-id="d5c7b-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="d5c7b-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="d5c7b-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="d5c7b-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="d5c7b-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5c7b-212"><em>Seguimiento</em></span><span class="sxs-lookup"><span data-stu-id="d5c7b-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="d5c7b-213">Especifica las opciones de seguimiento utilizadas en el seguimiento del enrutamiento de Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="d5c7b-214">Valores aceptables:</span><span class="sxs-lookup"><span data-stu-id="d5c7b-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5c7b-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="d5c7b-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="d5c7b-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="d5c7b-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d5c7b-217">El conjunto completo de funciones del SDK administrativo de COM+ está disponible mediante objetos COM.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="d5c7b-218">Esto permite que cualquier programa Inicie y detenga las aplicaciones COM+ según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="d5c7b-219">Cuando se inicia una aplicación COM+, se trata de la aplicación que se está ejecutando, no de los componentes individuales dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="d5c7b-220">Si una aplicación llama a un componente que no está en cola, se inicia la aplicación COM+ que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="d5c7b-221">Si la casilla del agente de escucha está habilitada, el agente de escucha también se inicia y comienza el procesamiento de mensajes para los componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="d5c7b-222">Aunque el servicio de componentes en cola puede iniciarse de esta manera, si empaqueta componentes en cola y no en cola en una sola aplicación COM+, asegúrese de que realmente desea que los componentes en cola se inicien si se ejecuta un componente sin cola.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="d5c7b-223">Si no es así, empaquete los componentes en cola en una aplicación COM+ independiente de los demás componentes.</span><span class="sxs-lookup"><span data-stu-id="d5c7b-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d5c7b-224">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5c7b-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c7b-225">Activación de colas de componentes</span><span class="sxs-lookup"><span data-stu-id="d5c7b-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




