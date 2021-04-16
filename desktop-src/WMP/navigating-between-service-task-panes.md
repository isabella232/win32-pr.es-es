---
title: Desplazarse entre los paneles de tareas de servicio
description: Desplazarse entre los paneles de tareas de servicio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player tiendas en línea, navegar
- tiendas en línea, navegar
- Escriba 2 tiendas en línea, navegación
- Windows Media Player tiendas en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Windows Media Player tiendas en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tipo 2 tiendas en línea, paneles de tareas
- navegar por las tiendas en línea de tipo 2
- Media Player de Windows, paneles de tareas de servicio
- Media Player de Windows, paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357098"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="e2f37-116">Desplazarse entre los paneles de tareas de servicio</span><span class="sxs-lookup"><span data-stu-id="e2f37-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="e2f37-117">Para desplazarse entre los paneles de tareas de servicio de Windows Media Player, use el método **NavigateTaskPaneURL** , que está disponible mediante el objeto **window. external** .</span><span class="sxs-lookup"><span data-stu-id="e2f37-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="e2f37-118">Cuando se usa este método, se especifican valores para tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="e2f37-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="e2f37-119">*bstrKeyName*.</span><span class="sxs-lookup"><span data-stu-id="e2f37-119">*bstrKeyName*.</span></span> <span data-ttu-id="e2f37-120">Este es el nombre de la clave de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e2f37-120">This is the key name of the online store.</span></span> <span data-ttu-id="e2f37-121">Al navegar en una tienda en línea, use el nombre de clave del almacén actual.</span><span class="sxs-lookup"><span data-stu-id="e2f37-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="e2f37-122">*bstrTaskPane*.</span><span class="sxs-lookup"><span data-stu-id="e2f37-122">*bstrTaskPane*.</span></span> <span data-ttu-id="e2f37-123">Esta cadena contiene el nombre del panel de tareas de servicio al que desea desplazarse.</span><span class="sxs-lookup"><span data-stu-id="e2f37-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="e2f37-124">*bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="e2f37-124">*bstrParams*.</span></span> <span data-ttu-id="e2f37-125">Esta cadena contiene los parámetros de cadena de consulta que desea anexar a la dirección URL de la página web hospedada por el panel de tareas de servicio al que desea desplazarse.</span><span class="sxs-lookup"><span data-stu-id="e2f37-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="e2f37-126">La navegación se administra mediante una página web que se crea, denominada página navegar.</span><span class="sxs-lookup"><span data-stu-id="e2f37-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="e2f37-127">La dirección URL de la página navegar se especifica mediante el elemento **Navigate** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="e2f37-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="e2f37-128">Cuando se llama a **NavigateTaskPaneURL**, Windows Media Player abre la página navegar, no la Página Web especificada por los elementos **ServiceTask1**, **ServiceTask2** o **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="e2f37-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="e2f37-129">Es la página de navegación que recibe la cadena de consulta especificada por *bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="e2f37-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="e2f37-130">La página navegar debe contener las reglas que determinan el contenido que se muestra en un panel de tareas de servicio después de la navegación.</span><span class="sxs-lookup"><span data-stu-id="e2f37-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="e2f37-131">Por ejemplo, supongamos que quiere que los usuarios haga clic en un vínculo para navegar de **ServiceTask1** a **ServiceTask2**.</span><span class="sxs-lookup"><span data-stu-id="e2f37-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="e2f37-132">Puede usar el siguiente código HTML para crear el vínculo:</span><span class="sxs-lookup"><span data-stu-id="e2f37-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="e2f37-133">Cuando el usuario hace clic en el vínculo de vídeo, Windows Media Player cambia a **ServiceTask2** y abre la página navegar, anexando la siguiente cadena de consulta a su dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e2f37-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="e2f37-134">El parámetro from identifica la página desde la que el usuario hizo clic en el vínculo y el parámetro to identifica el número del panel de tareas de servicio al que desea navegar.</span><span class="sxs-lookup"><span data-stu-id="e2f37-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="e2f37-135">(Tenga en cuenta que no hay nada especial sobre estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="e2f37-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="e2f37-136">Puede usar los parámetros que desee para cualquier propósito que elija).</span><span class="sxs-lookup"><span data-stu-id="e2f37-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="e2f37-137">Por ejemplo, en el ejemplo de código siguiente se muestra el elemento **Navigate** en un documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="e2f37-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="e2f37-138">La dirección URL resultante, completa con la cadena de consulta, se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e2f37-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="e2f37-139">En el ejemplo de código siguiente se muestra la página navegar:</span><span class="sxs-lookup"><span data-stu-id="e2f37-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="e2f37-140">El código anterior simplemente crea una dirección URL y redirige el explorador a ella.</span><span class="sxs-lookup"><span data-stu-id="e2f37-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="e2f37-141">En primer lugar, el código recupera los valores de la cadena de consulta de la dirección URL y la propia cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="e2f37-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="e2f37-142">Usa el valor del parámetro to para determinar la página que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="e2f37-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="e2f37-143">A continuación, anexa la cadena de consulta original a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e2f37-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="e2f37-144">Por último, navega por el explorador con una dirección URL similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e2f37-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="e2f37-145">Siempre que realice la navegación de esta manera, asegúrese de especificar [external. SelectedTaskPane](external-selectedtaskpane.md) para asegurarse de que el botón de tarea correcto esté resaltado.</span><span class="sxs-lookup"><span data-stu-id="e2f37-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="e2f37-146">**ADVERTENCIA** de Tenga cuidado con el uso de parámetros de cadena de consulta para la navegación.</span><span class="sxs-lookup"><span data-stu-id="e2f37-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="e2f37-147">Cualquier persona que cree una lista de reproducción de ASX puede proporcionar páginas web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="e2f37-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="e2f37-148">Esto significa que los sitios Web malintencionados pueden pasar valores de cadena de consulta a la tienda en línea mediante **NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="e2f37-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="e2f37-149">Debe planear esta posibilidad para proteger la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e2f37-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="e2f37-150">Por ejemplo, si la tienda en línea simplemente muestra un valor de cadena de consulta para el usuario, un sitio Web malintencionado podría mostrar texto inesperado.</span><span class="sxs-lookup"><span data-stu-id="e2f37-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2f37-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2f37-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f37-152">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e2f37-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="e2f37-153">**Elemento Navigate**</span><span class="sxs-lookup"><span data-stu-id="e2f37-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="e2f37-154">**Navegación para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="e2f37-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




