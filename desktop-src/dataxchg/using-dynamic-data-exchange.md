---
title: Usar Intercambio dinámico de datos
description: En este tema se proporcionan ejemplos de código relacionados con el intercambio dinámico de datos.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Intercambio dinámico de datos (DDE), conversaciones
- DDE (Intercambio dinámico de datos), conversaciones
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), ejemplos
- DDE (Intercambio dinámico de datos), ejemplos
- Intercambio dinámico de datos (DDE), comandos de aplicaciones de servidor
- DDE (Intercambio dinámico de datos), comandos en aplicaciones de servidor
- Intercambio dinámico de datos (DDE), vínculos de datos
- DDE (Intercambio dinámico de datos), vínculos de datos
- Intercambio dinámico de datos (DDE), elementos
- DDE (Intercambio dinámico de datos), elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359083"
---
# <a name="using-dynamic-data-exchange"></a>Usar Intercambio dinámico de datos

Esta sección contiene ejemplos de código sobre las siguientes tareas:

-   [Iniciar una conversación](#initiating-a-conversation)
-   [Transferir un solo elemento](#transferring-a-single-item)
    -   [Recuperación de un elemento del servidor](#retrieving-an-item-from-the-server)
    -   [Envío de un elemento al servidor](#submitting-an-item-to-the-server)
-   [Establecer un vínculo de datos permanente](#establishing-a-permanent-data-link)
    -   [Iniciar un vínculo de datos](#initiating-a-data-link)
    -   [Iniciar un vínculo de datos con el comando pegar vínculo](#initiating-a-data-link-with-the-paste-link-command)
    -   [Notificación al cliente de que los datos han cambiado](#notifying-the-client-that-data-has-changed)
    -   [Finalización de un vínculo de datos](#terminating-a-data-link)
-   [Ejecutar comandos en una aplicación de servidor](#carrying-out-commands-in-a-server-application)
-   [Finalizar una conversación](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Iniciar una conversación

Para iniciar una conversación Intercambio dinámico de datos (DDE), el cliente envía un mensaje de [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md) . Normalmente, el cliente difunde este mensaje mediante una llamada a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), con – 1 como primer parámetro. Si la aplicación ya tiene el identificador de ventana de la aplicación de servidor, puede enviar el mensaje directamente a esa ventana. El cliente prepara los átomos para el nombre de la aplicación y el nombre del tema mediante una llamada a [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma). El cliente puede solicitar conversaciones con cualquier posible aplicación de servidor y para cualquier tema potencial proporcionando átomos **null** (comodín) para la aplicación y el tema.

En el ejemplo siguiente se muestra cómo el cliente inicia una conversación, donde se especifican tanto la aplicación como el tema.


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> Si la aplicación usa átomos **null** , no es necesario usar las funciones [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) y [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) . En este ejemplo, la aplicación cliente crea dos átomos globales que contienen el nombre del servidor y el nombre del tema, respectivamente.

 

La aplicación cliente envía un mensaje de [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md) con estos dos átomos en el parámetro *lParam* del mensaje. En la llamada a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , el identificador de ventana especial – 1 indica al sistema que envíe este mensaje a todas las demás aplicaciones activas. **SendMessage** no vuelve a la aplicación cliente hasta que todas las aplicaciones que reciben el mensaje, a su vez, devuelven el control al sistema. Esto significa que se garantiza que el cliente ha procesado todos los mensajes de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) enviados en respuesta por las aplicaciones del servidor en el momento en que se devuelve la llamada **SendMessage** .

Una vez que [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve, la aplicación cliente elimina los átomos globales.

Las aplicaciones de servidor responden según la lógica que se muestra en el diagrama siguiente.

![lógica de respuesta de la aplicación de servidor](images/csdde-01.png)

Para confirmar uno o más temas, el servidor debe crear átomos para cada conversación (requiere átomos de nombre de aplicación duplicados si hay varios temas) y enviar un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para cada conversación, como se muestra en el ejemplo siguiente.


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



Cuando un servidor responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) , la aplicación cliente debe guardar un identificador en la ventana del servidor. El cliente que recibe el identificador como el parámetro *wParam* del mensaje de **confirmación de \_ DDE \_ de WM** envía entonces todos los mensajes DDE subsiguientes a la ventana del servidor que identifica.

Si la aplicación cliente usa un átomo **nulo** para el nombre de la aplicación o el nombre del tema, se espera que la aplicación reciba confirmaciones de más de una aplicación de servidor. Varias confirmaciones también pueden provienen de varias instancias de un servidor DDE, incluso si la aplicación cliente no **es null** usar átomos. Un servidor siempre debe usar una ventana única para cada conversación. El procedimiento de ventana de la aplicación cliente puede usar un identificador de la ventana del servidor (que se proporciona como el parámetro *lParam* de [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)) para realizar el seguimiento de varias conversaciones. Esto permite que una sola ventana de cliente procese varias conversaciones sin necesidad de finalizar y volver a conectar con una nueva ventana de cliente para cada conversación.

## <a name="transferring-a-single-item"></a>Transferir un solo elemento

Una vez establecida una conversación DDE, el cliente puede recuperar el valor de un elemento de datos del servidor emitiendo el mensaje de solicitud de [**WM \_ DDE \_**](wm-dde-request.md) o enviar un valor de elemento de datos al servidor emitiendo [**WM \_ DDE \_**](wm-dde-poke.md).

-   [Recuperación de un elemento del servidor](#retrieving-an-item-from-the-server)
-   [Envío de un elemento al servidor](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Recuperación de un elemento del servidor

Para recuperar un elemento del servidor, el cliente envía al servidor un mensaje [**de \_ \_ solicitud de DDE de WM**](wm-dde-request.md) que especifica el elemento y el formato que se va a recuperar, tal como se muestra en el ejemplo siguiente.


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



En este ejemplo, el cliente especifica el formato del portapapeles para el **\_ texto CF** como el formato preferido para el elemento de datos solicitado.

El receptor (servidor) del mensaje [**de \_ \_ solicitud de DDE de WM**](wm-dde-request.md) normalmente debe eliminar el elemento Atom, pero si se produce un error en la llamada [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , el cliente debe eliminar el átomo.

Si el servidor tiene acceso al elemento solicitado y puede representarlo en el formato solicitado, el servidor copia el valor del elemento como un objeto de memoria compartida y envía al cliente un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) , tal como se muestra en el ejemplo siguiente.


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



En este ejemplo, la aplicación de servidor asigna un objeto de memoria para que contenga el elemento de datos. El objeto de datos se inicializa como una estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .

A continuación, la aplicación de servidor establece el miembro **cfFormat** de la estructura en el \_ texto CF para informar a la aplicación cliente de que los datos están en formato de texto. El cliente responde copiando el valor de los datos solicitados en el miembro de **valor** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) . Una vez que el servidor ha rellenado el objeto de datos, el servidor Desbloquea los datos y crea un átomo global que contiene el nombre del elemento de datos.

Por último, el servidor emite el mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) llamando a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). El identificador del objeto de datos y el átomo que contiene el nombre del elemento se empaquetan en el parámetro *lParam* del mensaje mediante la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .

Si se produce un error en [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , el servidor debe utilizar la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) para liberar el parámetro *lParam* empaquetado. El servidor también debe liberar el parámetro *lParam* empaquetado para el mensaje de [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) que recibió.

Si el servidor no puede satisfacer la solicitud, envía un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo al cliente, tal y como se muestra en el ejemplo siguiente.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



Al recibir un mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) , el cliente procesa el valor del elemento de datos según corresponda. Después, si el miembro de **fAckReq** al que se apunta en el mensaje de **\_ \_ datos DDE de WM** es 1, el cliente debe enviar al servidor un mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo, como se muestra en el ejemplo siguiente.


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



En este ejemplo, el cliente examina el formato de los datos. Si el formato no es **el \_ texto CF** (o si el cliente no puede bloquear la memoria de los datos), el cliente envía un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo para indicar que no puede procesar los datos. Si el cliente no puede bloquear un identificador de datos porque el identificador contiene el miembro **fAckReq** , el cliente no debería enviar un mensaje de **\_ \_ confirmación DDE de WM** negativo. En su lugar, el cliente debe finalizar la conversación.

Si un cliente envía una confirmación negativa en respuesta a un mensaje de [**\_ \_ datos de DDE de WM**](wm-dde-data.md) , el servidor es responsable de liberar la memoria (pero no el parámetro *lParam* ) a la que hace referencia el mensaje de **\_ \_ datos de DDE de WM** asociado a la confirmación negativa.

Si puede procesar los datos, el cliente examina el miembro **fAckReq** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) para determinar si el servidor ha solicitado que se le informará de que el cliente ha recibido y procesado los datos correctamente. Si el servidor solicitó esta información, el cliente envía al servidor un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo.

Dado que el desbloqueo de datos invalida el puntero a los datos, el cliente guarda el valor del miembro **fRelease** antes de desbloquear el objeto de datos. Después de guardar el valor, el cliente lo examina para determinar si la aplicación de servidor solicitó al cliente liberar la memoria que contiene los datos. el cliente actúa en consecuencia.

Al recibir un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, el cliente puede pedir el mismo valor de elemento de nuevo, especificando un formato de Portapapeles diferente. Normalmente, un cliente solicitará primero el formato más complejo que pueda admitir y, a continuación, devolverá el paso abajo si es necesario a través de formatos progresivamente más sencillos hasta encontrar uno que el servidor pueda proporcionar.

Si el servidor admite el elemento formatos del tema sistema, el cliente puede determinar una vez qué formatos del portapapeles admite el servidor, en lugar de determinarlos cada vez que el cliente solicita un elemento.

### <a name="submitting-an-item-to-the-server"></a>Envío de un elemento al servidor

El cliente puede enviar un valor de elemento al servidor mediante el mensaje de anuncio de [**\_ \_ DDE de WM**](wm-dde-poke.md) . El cliente representa el elemento que se va a enviar y envía el mensaje de anuncio de **WM \_ DDE \_** , tal y como se muestra en el ejemplo siguiente.


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> El envío de datos mediante el uso de un mensaje de la función de correo de datos [**\_ DDE \_ de WM**](wm-dde-poke.md) es esencialmente el mismo que el envío mediante [**\_ \_ datos DDE de WM**](wm-dde-data.md), excepto que se envía el mensaje de correo de **WM \_ DDE \_** a través del cliente al servidor.

 

Si el servidor puede aceptar el valor del elemento de datos en el formato representado por el cliente, el servidor procesa el valor del elemento según corresponda y envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo. Si no puede procesar el valor del elemento, debido a su formato o por otros motivos, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



En este ejemplo, el servidor llama a [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar el nombre del elemento enviado por el cliente. A continuación, el servidor determina si admite el elemento y si el elemento se representa en el formato correcto (es decir, el \_ texto CF). Si el elemento no se admite y no se representa en el formato correcto, o si el servidor no puede bloquear la memoria de los datos, el servidor envía una confirmación negativa de nuevo a la aplicación cliente. Tenga en cuenta que, en este caso, el envío de una confirmación negativa es correcto porque siempre se supone que los mensajes de salida de la [**\_ DDE \_ de WM**](wm-dde-poke.md) tienen el conjunto de miembros **fAckReq** . El servidor debe omitir el miembro.

Si un servidor envía una confirmación negativa en respuesta a un mensaje de salida de [**WM \_ DDE \_**](wm-dde-poke.md) , el cliente es responsable de liberar la memoria (pero no el parámetro *lParam* ) al que hace referencia el mensaje de salida de **\_ DDE \_ de WM** asociado a la confirmación negativa.

## <a name="establishing-a-permanent-data-link"></a>Establecer un vínculo de datos permanente

Una aplicación cliente puede utilizar DDE para establecer un vínculo a un elemento de una aplicación de servidor. Después de establecer este tipo de vínculo, el servidor envía actualizaciones periódicas del elemento vinculado al cliente, normalmente, siempre que cambia el valor del elemento. Por lo tanto, se establece un flujo de datos permanente entre las dos aplicaciones: Este flujo de datos permanece en vigor hasta que se desconecta explícitamente.

### <a name="initiating-a-data-link"></a>Iniciar un vínculo de datos

El cliente inicia un vínculo de datos mediante la publicación de un mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) , tal como se muestra en el ejemplo siguiente.


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



En este ejemplo, la aplicación cliente establece la marca **fDeferUpd** del mensaje [**de \_ \_ aviso de DDE de WM**](wm-dde-advise.md) en **false**. Esto indica a la aplicación de servidor que envíe los datos al cliente cada vez que cambien los datos.

Si el servidor no puede dar servicio a la solicitud de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) , envía al cliente un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo. Pero si el servidor tiene acceso al elemento y puede representarlo en el formato solicitado, el servidor anota el nuevo vínculo (recuperando las marcas especificadas en el parámetro *hOptions* ) y envía al cliente un mensaje **de \_ \_ confirmación DDE de WM** positivo. A partir de ese momento, hasta que el cliente emita un mensaje de [**\_ \_ desaconsejaje de WM DDE**](wm-dde-unadvise.md) que coincida, el servidor enviará los datos nuevos al cliente cada vez que cambie el valor del elemento en el servidor.

El mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) establece el formato de los datos que se intercambiarán durante el vínculo. Si el cliente intenta establecer otro vínculo con el mismo elemento pero usa un formato de datos diferente, el servidor puede decidir rechazar el segundo formato de datos o intentar admitirlo. Si se ha establecido un vínculo activo para cualquier elemento de datos, el servidor solo puede admitir un formato de datos cada vez. Esto se debe a que el mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) para un vínculo cálido tiene un identificador de datos **nulo** que, de lo contrario, contiene la información de formato. Por lo tanto, un servidor debe rechazar todos los vínculos cálidos de un elemento ya vinculado y debe rechazar todos los vínculos de un elemento que tenga vínculos cálidos. Otra interpretación puede ser que el servidor cambie el formato y el estado activo o activo de un vínculo cuando se solicite un segundo vínculo para el mismo elemento de datos.

En general, las aplicaciones cliente no deben intentar establecer más de un vínculo a la vez para un elemento de datos.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Iniciar un vínculo de datos con el comando pegar vínculo

Las aplicaciones que admiten vínculos de datos activos o semiactivos suelen admitir un formato de Portapapeles registrado denominado Link. Cuando se asocian a los comandos de copiar y pegar vínculo de la aplicación, este formato del portapapeles permite al usuario establecer conversaciones DDE entre aplicaciones con solo copiar un elemento de datos en la aplicación de servidor y pegarlo en la aplicación cliente.

Una aplicación de servidor admite el formato del Portapapeles del vínculo colocando en el portapapeles una cadena que contiene la aplicación, el tema y los nombres de elemento cuando el usuario elige el comando **copiar** en el menú **edición** . A continuación se encuentra el formato de vínculo estándar:

*aplicación ***\\ 0*** tema ***\\ 0*** elemento * * * \\ 0 \\ 0**

Un solo carácter nulo separa los nombres y dos caracteres nulos terminan toda la cadena.

Las aplicaciones cliente y servidor deben registrar el formato del Portapapeles del vínculo, como se muestra a continuación:


```
cfLink = RegisterClipboardFormat("Link");
```



Una aplicación cliente admite el formato del Portapapeles del vínculo por medio de un comando pegar vínculo en el menú edición. Cuando el usuario elige este comando, la aplicación cliente analiza los nombres de aplicación, tema y elemento de los datos del Portapapeles con formato de vínculo. Con estos nombres, la aplicación cliente inicia una conversación para la aplicación y el tema, si tal conversación no existe todavía. A continuación, la aplicación cliente envía un mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) a la aplicación de servidor, especificando el nombre del elemento contenido en los datos del Portapapeles con formato de vínculo.

A continuación se puede obtener un ejemplo de la respuesta de una aplicación cliente cuando el usuario elige el comando pegar vínculo.


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



En este ejemplo, la aplicación cliente abre el portapapeles y determina si contiene datos en el formato de vínculo (es decir, cfLink) que se había registrado previamente. Si no es así, o si no puede bloquear los datos en el portapapeles, el cliente devuelve.

Una vez que la aplicación cliente recupera un puntero a los datos del portapapeles, analiza los datos para extraer la aplicación, el tema y los nombres de los elementos.

La aplicación cliente determina si ya existe una conversación en el tema entre ella y la aplicación de servidor. Si existe una conversación, el cliente comprueba si ya existe un vínculo para el elemento de datos. Si existe este tipo de vínculo, el cliente muestra un cuadro de mensaje al usuario; de lo contrario, llama a su propia función *SendAdvise* para enviar un mensaje de [**aviso de WM \_ DDE \_**](wm-dde-advise.md) al servidor para el elemento.

Si no existe ya una conversación en el tema entre el cliente y el servidor, el cliente llama primero a su propia función *SendInitiate* para difundir el mensaje de [**Inicio de WM \_ \_ DDE**](wm-dde-initiate.md) para solicitar una conversación y, en segundo lugar, llama a su propia función *FindServerGivenAppTopic* para establecer la conversación con la ventana que responde en nombre de la aplicación de servidor. Una vez iniciada la conversación, la aplicación cliente llama a *SendAdvise* para solicitar el vínculo.

### <a name="notifying-the-client-that-data-has-changed"></a>Notificación al cliente de que los datos han cambiado

Cuando el cliente establece un vínculo con el mensaje [**de \_ \_ aviso de DDE de WM**](wm-dde-advise.md) , con el miembro **fDeferUpd** no establecido (es decir, igual a cero) en la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , el cliente ha solicitado al servidor que envíe el elemento de datos cada vez que cambie el valor del elemento. En tales casos, el servidor representa el nuevo valor del elemento de datos en el formato especificado previamente y envía al cliente un mensaje [**de \_ \_ datos de WM DDE**](wm-dde-data.md) , tal como se muestra en el ejemplo siguiente.


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



En este ejemplo, el cliente procesa el valor del elemento según corresponda. Si se establece la marca **fAckReq** para el elemento, el cliente envía al servidor un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo.

Cuando el cliente establece el vínculo con el conjunto de miembros **fDeferUpd** (es decir, es igual a 1), el cliente ha solicitado que solo se envíe una notificación, no los datos en sí, cada vez que cambien los datos. En tales casos, cuando el valor del elemento cambia, el servidor no representa el valor, sino que simplemente envía el cliente a un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) con un identificador de datos null, como se muestra en el ejemplo siguiente.


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



Según sea necesario, el cliente puede solicitar el valor más reciente del elemento de datos mediante la emisión de un mensaje de [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) normal o simplemente pasar por alto el aviso del servidor de que los datos han cambiado. En cualquier caso, si **fAckReq** es igual a 1, se espera que el cliente envíe un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo al servidor.

### <a name="terminating-a-data-link"></a>Finalización de un vínculo de datos

Si el cliente solicita que se termine un vínculo de datos específico, el cliente envía al servidor un mensaje de [**\_ \_ desaconsejad DDE de WM**](wm-dde-unadvise.md) , tal como se muestra en el ejemplo siguiente.


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



El servidor comprueba si el cliente tiene actualmente un vínculo al elemento específico en esta conversación. Si existe un vínculo, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; el servidor ya no es necesario para enviar actualizaciones sobre el elemento. Si no existe ningún vínculo, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.

El mensaje de [**\_ \_ desaconsejar DDE de WM**](wm-dde-unadvise.md) especifica un formato de datos. Un formato de cero informa al servidor de que detenga todos los vínculos del elemento especificado, incluso si se establecen varios vínculos activos y cada uno de ellos usa un formato diferente.

Para finalizar todos los vínculos de una conversación, la aplicación cliente envía el mensaje [**de \_ \_ desaconsejar DDE de WM**](wm-dde-unadvise.md) al servidor con un átomo de elemento nulo. El servidor determina si la conversación tiene al menos un vínculo establecido actualmente. Si existe un vínculo, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; el servidor deja de tener que enviar actualizaciones en la conversación. Si no existe ningún vínculo, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.

## <a name="carrying-out-commands-in-a-server-application"></a>Ejecutar comandos en una aplicación de servidor

Las aplicaciones pueden usar el mensaje de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) para hacer que un comando o una serie de comandos determinados se lleven a cabo en otra aplicación. Para ello, el cliente envía un mensaje de **\_ \_ ejecución de WM DDE** de servidor que contiene un identificador a una cadena de comandos, tal y como se muestra en el ejemplo siguiente.


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



En este ejemplo, el servidor intenta llevar a cabo la cadena de comandos especificada. Si se realiza correctamente, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; de lo contrario, envía un mensaje de **\_ \_ confirmación DDE de WM** negativo. Este mensaje de **\_ \_ confirmación de DDE de WM** reutiliza el identificador *hCommand* pasado en el mensaje de [**ejecución de WM \_ DDE \_**](wm-dde-execute.md) original.

Si la cadena de ejecución del comando del cliente solicita que el servidor finalice, el servidor debe responder mediante el envío de un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo y después publicar un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) antes de finalizar. El resto de los comandos que se envían con un mensaje de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) deben ejecutarse sincrónicamente; es decir, el servidor debería enviar un mensaje de **\_ \_ confirmación de WM DDE** solo después de completar correctamente el comando.

## <a name="terminating-a-conversation"></a>Finalizar una conversación

Tanto el cliente como el servidor pueden emitir un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) para finalizar una conversación en cualquier momento. Del mismo modo, las aplicaciones cliente y servidor deben estar preparadas para recibir este mensaje en cualquier momento. Una aplicación debe finalizar todas sus conversaciones antes de cerrarse.

En el ejemplo siguiente, la aplicación que finaliza la conversación envía un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) .


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Esto informa a la otra aplicación de que la aplicación emisora no enviará más mensajes y el destinatario puede cerrar su ventana. En todos los casos, se espera que el destinatario responda rápidamente mediante el envío de un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) . El destinatario no debe enviar un mensaje de [**\_ \_ confirmación del DDE de WM**](wm-dde-ack.md) negativo, ocupado o positivo.

Una vez que una aplicación ha enviado el mensaje de [**\_ \_ terminación de WM DDE**](wm-dde-terminate.md) al asociado en una conversación DDE, no debe responder a los mensajes de ese asociado, ya que es posible que el socio haya destruido la ventana a la que se enviará la respuesta.

Si una aplicación recibe un mensaje DDE distinto de [**la \_ \_ terminación de WM DDE**](wm-dde-terminate.md) después de haber publicado la **terminación de WM \_ DDE \_**, debe liberar todos los objetos asociados a los mensajes recibidos, excepto los identificadores de datos para los mensajes de [**WM \_ DDE \_ Data**](wm-dde-data.md) o [**WM \_ DDE \_**](wm-dde-poke.md) , que **no** tienen el conjunto de miembros **fRelease** .

Cuando una aplicación está a punto de finalizar, debe terminar todas las conversaciones DDE activas antes de completar el procesamiento del mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) . Sin embargo, si una aplicación no finaliza sus conversaciones DDE activas, el sistema finalizará cualquier conversación DDE asociada a una ventana cuando se destruya la ventana. En el ejemplo siguiente se muestra cómo una aplicación de servidor finaliza todas las conversaciones DDE.


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 