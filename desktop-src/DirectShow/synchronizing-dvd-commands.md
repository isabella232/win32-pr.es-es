---
description: Sincronizar comandos de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizar comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678412"
---
# <a name="synchronizing-dvd-commands"></a>Sincronizar comandos de DVD

Los comandos de DVD no siempre se completan al instante. Por esta razón, algunos de los métodos de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) son asíncronos. Estos incluyen métodos de reproducción, como **PlayTitle**, y métodos de navegación de menú, como **showmenu** y **ReturnFromSubmenu**. Un método asincrónico se devuelve inmediatamente, sin esperar a que se complete el comando. Una vez que el método devuelve, otros eventos pueden impedir que el comando se complete, aunque el método se haya realizado correctamente. DirectShow proporciona varias opciones para sincronizar comandos, desde no sincronizar con la sincronización completa mediante eventos de gráfico de filtro.

Todos los métodos asincrónicos tienen un parámetro *dwFlags* y un parámetro *ppCmd* . El parámetro *dwFlags* especifica el comportamiento de sincronización y el parámetro *ppCmd* devuelve un puntero a un objeto de sincronización opcional. Se producirán diferentes comportamientos en función de los valores que se proporcionen para estos parámetros.

**Sin sincronización**

En el caso de una aplicación de reproducción de DVD básica, la mejor opción puede ser simplemente omitir los problemas de sincronización. En ocasiones, es posible que se produzca un error en un comando o que la interfaz de usuario se retrase ligeramente cuando se actualice, pero estos errores se encontrarán en el orden de fracciones de segundo.

Para emitir un comando sin sincronización, establezca la marca DVD \_ cmd \_ Flag \_ None en el parámetro *dwFlags* y establezca el parámetro *ppCmd* en **null**:


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Bloqueos**

Si establece la marca de \_ \_ \_ \_ bloqueo de marcador de cmd de DVD de EC en el parámetro *dwFlags* , el método se bloquea hasta que se completa el comando:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



En efecto, esta marca convierte un método asincrónico en un método sincrónico. El inconveniente es que la interfaz de usuario se bloquea si llama al método desde el subproceso de la aplicación.

**Synchronization (objeto)**

Todos los métodos asincrónicos pueden devolver un objeto de sincronización, que puede usar para esperar a que el comando se inicie o finalice. Para obtener este objeto, pase la dirección de un puntero [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) en el parámetro *ppCmd* :


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Si el método se ejecuta correctamente, devuelve un nuevo objeto **IDvdCmd** . El método [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) se bloquea hasta que se inicia el comando y el método [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) se bloquea hasta que finaliza el comando. El valor devuelto indica el estado del comando.

El código siguiente es funcionalmente equivalente a establecer la \_ marca de \_ bloqueo de marca cmd de DVD de EC \_ \_ , que se mostró anteriormente.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



En este caso, el método **PlayTitle** no se bloquea, pero la aplicación se bloquea llamando a **WaitForEnd**.

**Eventos de estado de comando**

Si establece la \_ \_ \_ marca SendEvents de la marca de cmd de DVD en el parámetro *dwFlags* , el navegador de DVD envía un evento de inicio de cmd de DVD de EC cuando se inicia el comando y un evento de fin de cmd de DVD de EC cuando finaliza el comando. [**\_ \_ \_**](ec-dvd-cmd-start.md) [**\_ \_ \_**](ec-dvd-cmd-end.md)

El parámetro *lParam2* del evento es el valor devuelto HRESULT para el comando. El parámetro *lParam1* del evento proporciona una manera de obtener el objeto de sincronización para el comando. Si pasa *lParam1* al método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , el método devuelve un puntero a la interfaz **IDvdCmd** del objeto de sincronización. Puede usar esta interfaz para esperar a que finalice el comando, como se describió anteriormente. Sin embargo, si se pasa **null** para el parámetro *ppCmd* en el método **IDvdControl2** original, el explorador de DVD no crea un objeto de sincronización y **GetCmdFromEvent** devuelve \_ un error.

En el código siguiente se muestra cómo usar eventos de estado de comandos sin ningún objeto de sincronización.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



Tenga en cuenta que, sin un objeto de sincronización, no se puede saber qué comando está asociado al evento. En el código siguiente se muestra cómo utilizar los eventos con el objeto de sincronización. La idea es almacenar los objetos de sincronización en una lista y, a continuación, comparar los punteros de objeto cuando se obtiene el evento de [**\_ \_ \_ Inicio**](ec-dvd-cmd-start.md) o el evento de [**\_ \_ \_ fin de CMD**](ec-dvd-cmd-end.md) de DVD de EC.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**Vaciar los búferes del explorador de DVD**

Durante la reproducción, el explorador de DVD almacena en búfer los datos de vídeo. La cantidad de datos almacenados en búfer varía. Cuando el navegador de DVD cambia a un nuevo fragmento de vídeo, los datos que ya están en la canalización no se pierden, por lo que la transición es fluida. De forma predeterminada, cuando el navegador de DVD emite un comando, no vacía los datos que ya se encuentren en la canalización. Como resultado, puede haber cierta latencia antes de que pueda ver el efecto del comando, en función de la cantidad de datos almacenados en búfer. Para aumentar la capacidad de respuesta, puede forzar el vaciado del navegador de DVD si establece la \_ \_ marca de vaciado de marca de cmd de DVD \_ .


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Esta marca se puede combinar con cualquiera de las marcas descritas anteriormente, mediante una operación OR bit a bit. Un efecto secundario del vaciado es que es posible que se pierda algún vídeo, por lo que no debe usar esta marca si necesita garantizar que no haya espacios en el vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



