---
title: Mantenimiento de la información de sesión
description: Mantenimiento de la información de sesión
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media en línea, mantener la información de sesión
- tiendas en línea, mantener la información de sesión
- tiendas en línea de tipo 2, mantener la información de sesión
- Reproductor de Windows Media en línea, información de sesión
- tiendas en línea, información de sesión
- tipo 2 tiendas en línea, información de sesión
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- mantener la información de sesión
- información de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b20bca3216f8e4a4247f513dccddf1cb155ef3c719ef104874e36da2bf6b018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135198"
---
# <a name="maintaining-session-information"></a>Mantenimiento de la información de sesión

## <a name="how-the-sample-stores-information"></a>Cómo almacena la información el ejemplo

La página web de ejemplo mantiene los datos mediante cookies. Las cookies son simplemente pares de nombre y valor persistentes que el explorador web puede almacenar automáticamente.

Cuando se cierra la página web, se **ejecuta la función Shutdown.** **Shutdown** llama a la **función SetPendingCookies.** Esta función recorre en bucle la lista de recopilación de descargas, almacenada en el cuadro de lista desplegable denominado selDLC. Si una colección de descarga contiene elementos incompletos, la función llama al **método SetCookie**, pasando un nombre y un valor. La cadena de nombre se determina anexando un valor entero a un valor constante, **WMPDLC**, que se almacena en la variable denominada g \_ sPreCookie. Por ejemplo, para la tercera recopilación de descargas pendiente, el nombre de la cookie sería "WMPDLC2", porque el mecanismo de recuento es de base cero. A medida que se crea cada cookie, la función incrementa la variable global g \_ Pending para mantener un recuento de descargas pendientes. El código se reproduce aquí para su comodidad:


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



**IsDLCComplete es una** función auxiliar que simplemente recorre en bucle cada elemento de descarga de la colección de descarga para determinar si hay algún elemento pendiente. Si hay un elemento pendiente, la función devuelve false.

**SetCookie** es la función que crea la cookie.

Cuando **se devuelve SetPendingCookies,** **Shutdown** crea la cookie count, que almacena el valor de la variable g \_ Pending. Este valor es importante porque la página web necesita una manera de determinar cuántas cookies recuperar cuando se vuelve a cargar. El nombre de la cookie count se almacena en la variable denominada g \_ sCountCookie.

## <a name="how-the-sample-retrieves-information"></a>Cómo recupera la información el ejemplo

Cuando se carga la página web, se ejecuta la función **Init.** En primer lugar, la función llama **a GetPendingDlCount para** recuperar la cookie de recuento. A continuación, almacena este valor en la variable denominada g \_ Pending. A continuación, llama a **la función PopulateDLList** para recuperar cada cookie de sesión de descarga y agregar su identificador al cuadro de lista desplegable. Este es el código de esa función:


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

A continuación, la función entra en un bucle. Cada nombre de cookie se construye como una cadena y, a continuación, la cookie se recupera mediante una llamada a la función auxiliar **GetCookie**. Una vez recuperada, la cookie se elimina mediante una llamada **a DelCookie**. Si la cookie tiene un valor, el valor se agrega al cuadro de lista. Esta acción inicia el evento **onChange** para la lista selDLC, que a su vez llama a la función de controlador **denominada OnSelectDLC**. Se trata de la misma función que se ejecuta cuando el usuario selecciona una colección de descarga; es el código que rellena el cuadro de lista de elementos de descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del Administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




