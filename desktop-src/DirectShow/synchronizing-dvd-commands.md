---
description: Sincronizar comandos de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizar comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38696425892618f1b66544e69a4a567d0f539234d991cb96792eda4f6f1509d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964815"
---
# <a name="synchronizing-dvd-commands"></a>Sincronizar comandos de DVD

Los comandos de DVD no siempre se completan al instante. Por este motivo, algunos de los métodos de [**IDvdControl2 son**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) asincrónicos. Estos incluyen métodos de reproducción, como **PlayTitle** y métodos de navegación de menús, como **ShowMenu** **y ReturnFromSubmenu.** Un método asincrónico devuelve inmediatamente, sin esperar a que se complete el comando. Después de que el método vuelva, otros eventos pueden impedir que el comando se complete, incluso si el método se ha completado correctamente. DirectShow proporciona varias opciones para sincronizar comandos, desde sin sincronización hasta sincronización completa mediante eventos de gráfico de filtros.

Todos los métodos asincrónicos tienen un *parámetro dwFlags* y un *parámetro ppCmd.* El *parámetro dwFlags* especifica el comportamiento de sincronización y el parámetro *ppCmd* devuelve un puntero a un objeto de sincronización opcional. Los distintos comportamientos se dan en función de los valores que se den para estos parámetros.

**Sin sincronización**

Para una aplicación de reproducción de DVD básica, la mejor opción puede ser simplemente omitir los problemas de sincronización. En ocasiones, un comando puede producir un error o la interfaz de usuario podría retraso ligeramente cuando se actualiza, pero estos errores estarán en el orden de fracciones de segundos.

Para emitir un comando sin sincronización, establezca la marca DVD CMD FLAG None en el parámetro \_ \_ \_ *dwFlags* y establezca el parámetro *ppCmd* en NULL :


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Bloqueos**

Si establece la marca EC DVD CMD FLAG Block en el parámetro \_ \_ \_ \_ *dwFlags,* el método se bloquea hasta que se completa el comando:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



En efecto, esta marca convierte un método asincrónico en un método sincrónico. El inconveniente es que la interfaz de usuario se bloquea si se llama al método desde el subproceso de aplicación.

**Objeto synchronization**

Todos los métodos asincrónicos pueden devolver un objeto de sincronización, que puede usar para esperar a que el comando se inicie o finalice. Para obtener este objeto, pase la dirección de un [**puntero IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) en el *parámetro ppCmd:*


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Si el método se realiza correctamente, devuelve un nuevo **objeto IDvdCmd.** El [**método IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) se bloquea hasta que comienza el comando y el método [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) se bloquea hasta que finaliza el comando. El valor devuelto indica el estado del comando.

El código siguiente es funcionalmente equivalente a establecer la marca \_ EC DVD CMD FLAG \_ \_ \_ Block, que se mostró anteriormente.


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



En este caso, el **método PlayTitle** no se bloquea, pero la aplicación se bloquea mediante una llamada **a WaitForEnd**.

**Eventos de estado del comando**

Si establece la marca DVD CMD FLAG SendEvents en el parámetro \_ \_ \_ *dwFlags,* [**\_ \_ \_**](ec-dvd-cmd-end.md) [**\_ \_ \_**](ec-dvd-cmd-start.md) el navegador de DVD envía un evento EC DVD CMD START cuando comienza el comando y un evento EC DVD CMD END cuando finaliza el comando.

El parámetro *lParam2 del* evento es el valor devuelto HRESULT del comando. El parámetro *lParam1 del* evento proporciona una manera de obtener el objeto de sincronización para el comando. Si pasa *lParam1* al método [**IDvdInfo2::GetCmdFromEvent,**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) el método devuelve un puntero a la interfaz **IDvdCmd** del objeto de sincronización. Puede usar esta interfaz para esperar a que se complete el comando, como se describió anteriormente. Sin embargo, si ha pasado **NULL** para el parámetro *ppCmd* en el método **IDvdControl2** original, el navegador de DVD no crea un objeto de sincronización y **GetCmdFromEvent** devuelve E \_ FAIL.

El código siguiente muestra cómo usar eventos de estado de comando sin ningún objeto de sincronización.


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



Tenga en cuenta que sin un objeto de sincronización, no se puede saber qué comando está asociado al evento. El código siguiente muestra cómo usar eventos con el objeto de sincronización. La idea es almacenar los objetos de sincronización en una lista y, a continuación, comparar punteros de objeto cuando se obtiene el evento [**\_ CMD \_ \_ START**](ec-dvd-cmd-start.md) o [**CMD \_ \_ \_ END de DVD**](ec-dvd-cmd-end.md) DE EC.


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



**Vaciar los búferes del navegador de DVD**

Durante la reproducción, el navegador de DVD almacena en búfer los datos de vídeo. La cantidad de datos almacenados en búfer varía. Cuando el navegador de DVD cambia a un nuevo fragmento de vídeo, los datos que ya están en la canalización no se pierden, por lo que la transición es perfecta. De forma predeterminada, cuando el navegador de DVD emite un comando, no vacía los datos que ya están en la canalización. Como resultado, puede haber cierta latencia antes de poder ver el efecto del comando, en función de la cantidad de datos almacenados en búfer. Para aumentar la capacidad de respuesta, puede forzar el vaciado del navegador de DVD estableciendo la marca \_ DVD CMD \_ FLAG \_ Flush.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Esta marca se puede combinar con cualquiera de las marcas descritas anteriormente, mediante un OR bit a bit. Un efecto secundario del vaciado es que se puede perder algún vídeo, por lo que no use esta marca si necesita garantizar que no haya espacios en el vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



