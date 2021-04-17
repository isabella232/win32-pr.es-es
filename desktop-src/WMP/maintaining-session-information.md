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
# <a name="maintaining-session-information"></a>Mantenimiento de la información de sesión

## <a name="how-the-sample-stores-information"></a>Cómo almacena la información el ejemplo

La Página Web de ejemplo mantiene los datos mediante cookies. Las cookies son simplemente pares de nombre/valor persistentes que puede almacenar el explorador Web automáticamente.

Cuando se cierra la página web, se ejecuta la función **Shutdown** . **Shutdown** llama a la función **SetPendingCookies**. Esta función recorre en bucle la lista de colecciones de descarga, que se almacena en el cuadro de lista desplegable denominado selDLC. Si una colección de descarga contiene elementos incompletos, la función llama al método **setcookie**, pasando un nombre y un valor. La cadena de nombre se determina anexando un valor entero a un valor constante, **WMPDLC**, que se almacena en la variable denominada g \_ sPreCookie. Por ejemplo, para la tercera colección de descargas pendientes, el nombre de la cookie sería "WMPDLC2", porque el mecanismo de recuento es de base cero. A medida que se crea cada cookie, la función incrementa la variable global g \_ pendiente para mantener un recuento de las descargas pendientes. El código se reproduce aquí para su comodidad:


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



**IsDLCComplete** es una función auxiliar que simplemente recorre en bucle cada elemento de descarga en la colección de descargas para determinar si hay algún elemento pendiente. Si hay un elemento pendiente, la función devuelve false.

**Setcookie** es la función que crea la cookie.

Cuando **SetPendingCookies** devuelve, **Shutdown** crea la cookie de recuento, que almacena el valor de la variable g \_ pendiente. Este valor es importante porque la página web necesita una manera de determinar el número de cookies que se van a recuperar cuando se recarga. El nombre de la cookie de recuento se almacena en la variable denominada g \_ sCountCookie.

## <a name="how-the-sample-retrieves-information"></a>Cómo recupera la información el ejemplo

Cuando se carga la página web, se ejecuta la función **init** . En primer lugar, la función llama a **GetPendingDlCount** para recuperar la cookie de recuento. A continuación, almacena este valor en la variable denominada g \_ Pending. A continuación, llama a la función **PopulateDLList** para recuperar cada cookie de sesión de descarga y agregar su identificador al cuadro de lista desplegable. Este es el código para esa función:


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



La función **ClearList** quita todos los elementos del cuadro de lista.

A continuación, la función entra en un bucle. Cada nombre de cookie se genera como una cadena y, a continuación, se recupera la cookie llamando a la función auxiliar **GetCookie**. Una vez recuperada, la cookie se elimina llamando a **DelCookie**. Si la cookie tiene un valor, el valor se agrega al cuadro de lista. Esta acción inicia el evento **onchange** para la lista selDLC, que a su vez llama a la función controladora denominada **OnSelectDLC**. Se trata de la misma función que se ejecuta cuando el usuario selecciona una colección de descarga; es el código que rellena el cuadro de lista descargar elemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




