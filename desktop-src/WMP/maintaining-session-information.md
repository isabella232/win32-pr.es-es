---
title: Mantenimiento de la información de sesión
description: Mantenimiento de la información de sesión
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, mantener la información de la sesión
- tiendas en línea, mantener la información de la sesión
- tipo 2 tiendas en línea, mantenimiento de la información de la sesión
- Windows Media Player tiendas en línea, información de sesión
- tiendas en línea, información de sesión
- tipo 2 tiendas en línea, información de sesión
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- mantenimiento de la información de sesión
- información de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357773"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="30c67-117">Mantenimiento de la información de sesión</span><span class="sxs-lookup"><span data-stu-id="30c67-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="30c67-118">Cómo almacena la información el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30c67-118">How the Sample Stores Information</span></span>

<span data-ttu-id="30c67-119">La Página Web de ejemplo mantiene los datos mediante cookies.</span><span class="sxs-lookup"><span data-stu-id="30c67-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="30c67-120">Las cookies son simplemente pares de nombre/valor persistentes que puede almacenar el explorador Web automáticamente.</span><span class="sxs-lookup"><span data-stu-id="30c67-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="30c67-121">Cuando se cierra la página web, se ejecuta la función **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="30c67-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="30c67-122">**Shutdown** llama a la función **SetPendingCookies**.</span><span class="sxs-lookup"><span data-stu-id="30c67-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="30c67-123">Esta función recorre en bucle la lista de colecciones de descarga, que se almacena en el cuadro de lista desplegable denominado selDLC.</span><span class="sxs-lookup"><span data-stu-id="30c67-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="30c67-124">Si una colección de descarga contiene elementos incompletos, la función llama al método **setcookie**, pasando un nombre y un valor.</span><span class="sxs-lookup"><span data-stu-id="30c67-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="30c67-125">La cadena de nombre se determina anexando un valor entero a un valor constante, **WMPDLC**, que se almacena en la variable denominada g \_ sPreCookie.</span><span class="sxs-lookup"><span data-stu-id="30c67-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="30c67-126">Por ejemplo, para la tercera colección de descargas pendientes, el nombre de la cookie sería "WMPDLC2", porque el mecanismo de recuento es de base cero.</span><span class="sxs-lookup"><span data-stu-id="30c67-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="30c67-127">A medida que se crea cada cookie, la función incrementa la variable global g \_ pendiente para mantener un recuento de las descargas pendientes.</span><span class="sxs-lookup"><span data-stu-id="30c67-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="30c67-128">El código se reproduce aquí para su comodidad:</span><span class="sxs-lookup"><span data-stu-id="30c67-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="30c67-129">**IsDLCComplete** es una función auxiliar que simplemente recorre en bucle cada elemento de descarga en la colección de descargas para determinar si hay algún elemento pendiente.</span><span class="sxs-lookup"><span data-stu-id="30c67-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="30c67-130">Si hay un elemento pendiente, la función devuelve false.</span><span class="sxs-lookup"><span data-stu-id="30c67-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="30c67-131">**Setcookie** es la función que crea la cookie.</span><span class="sxs-lookup"><span data-stu-id="30c67-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="30c67-132">Cuando **SetPendingCookies** devuelve, **Shutdown** crea la cookie de recuento, que almacena el valor de la variable g \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="30c67-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="30c67-133">Este valor es importante porque la página web necesita una manera de determinar el número de cookies que se van a recuperar cuando se recarga.</span><span class="sxs-lookup"><span data-stu-id="30c67-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="30c67-134">El nombre de la cookie de recuento se almacena en la variable denominada g \_ sCountCookie.</span><span class="sxs-lookup"><span data-stu-id="30c67-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="30c67-135">Cómo recupera la información el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30c67-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="30c67-136">Cuando se carga la página web, se ejecuta la función **init** .</span><span class="sxs-lookup"><span data-stu-id="30c67-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="30c67-137">En primer lugar, la función llama a **GetPendingDlCount** para recuperar la cookie de recuento.</span><span class="sxs-lookup"><span data-stu-id="30c67-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="30c67-138">A continuación, almacena este valor en la variable denominada g \_ Pending.</span><span class="sxs-lookup"><span data-stu-id="30c67-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="30c67-139">A continuación, llama a la función **PopulateDLList** para recuperar cada cookie de sesión de descarga y agregar su identificador al cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="30c67-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="30c67-140">Este es el código para esa función:</span><span class="sxs-lookup"><span data-stu-id="30c67-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="30c67-141">La función **ClearList** quita todos los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="30c67-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="30c67-142">A continuación, la función entra en un bucle.</span><span class="sxs-lookup"><span data-stu-id="30c67-142">The function then enters a loop.</span></span> <span data-ttu-id="30c67-143">Cada nombre de cookie se genera como una cadena y, a continuación, se recupera la cookie llamando a la función auxiliar **GetCookie**.</span><span class="sxs-lookup"><span data-stu-id="30c67-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="30c67-144">Una vez recuperada, la cookie se elimina llamando a **DelCookie**.</span><span class="sxs-lookup"><span data-stu-id="30c67-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="30c67-145">Si la cookie tiene un valor, el valor se agrega al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="30c67-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="30c67-146">Esta acción inicia el evento **onchange** para la lista selDLC, que a su vez llama a la función controladora denominada **OnSelectDLC**.</span><span class="sxs-lookup"><span data-stu-id="30c67-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="30c67-147">Se trata de la misma función que se ejecuta cuando el usuario selecciona una colección de descarga; es el código que rellena el cuadro de lista descargar elemento.</span><span class="sxs-lookup"><span data-stu-id="30c67-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30c67-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30c67-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c67-149">**Uso del administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="30c67-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




