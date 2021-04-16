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
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="57dba-103">Sincronizar comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="57dba-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="57dba-104">Los comandos de DVD no siempre se completan al instante.</span><span class="sxs-lookup"><span data-stu-id="57dba-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="57dba-105">Por esta razón, algunos de los métodos de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="57dba-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="57dba-106">Estos incluyen métodos de reproducción, como **PlayTitle**, y métodos de navegación de menú, como **showmenu** y **ReturnFromSubmenu**.</span><span class="sxs-lookup"><span data-stu-id="57dba-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="57dba-107">Un método asincrónico se devuelve inmediatamente, sin esperar a que se complete el comando.</span><span class="sxs-lookup"><span data-stu-id="57dba-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="57dba-108">Una vez que el método devuelve, otros eventos pueden impedir que el comando se complete, aunque el método se haya realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="57dba-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="57dba-109">DirectShow proporciona varias opciones para sincronizar comandos, desde no sincronizar con la sincronización completa mediante eventos de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="57dba-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="57dba-110">Todos los métodos asincrónicos tienen un parámetro *dwFlags* y un parámetro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="57dba-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="57dba-111">El parámetro *dwFlags* especifica el comportamiento de sincronización y el parámetro *ppCmd* devuelve un puntero a un objeto de sincronización opcional.</span><span class="sxs-lookup"><span data-stu-id="57dba-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="57dba-112">Se producirán diferentes comportamientos en función de los valores que se proporcionen para estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="57dba-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="57dba-113">**Sin sincronización**</span><span class="sxs-lookup"><span data-stu-id="57dba-113">**No Synchronization**</span></span>

<span data-ttu-id="57dba-114">En el caso de una aplicación de reproducción de DVD básica, la mejor opción puede ser simplemente omitir los problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="57dba-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="57dba-115">En ocasiones, es posible que se produzca un error en un comando o que la interfaz de usuario se retrase ligeramente cuando se actualice, pero estos errores se encontrarán en el orden de fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="57dba-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="57dba-116">Para emitir un comando sin sincronización, establezca la marca DVD \_ cmd \_ Flag \_ None en el parámetro *dwFlags* y establezca el parámetro *ppCmd* en **null**:</span><span class="sxs-lookup"><span data-stu-id="57dba-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="57dba-117">**Bloqueos**</span><span class="sxs-lookup"><span data-stu-id="57dba-117">**Blocking**</span></span>

<span data-ttu-id="57dba-118">Si establece la marca de \_ \_ \_ \_ bloqueo de marcador de cmd de DVD de EC en el parámetro *dwFlags* , el método se bloquea hasta que se completa el comando:</span><span class="sxs-lookup"><span data-stu-id="57dba-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="57dba-119">En efecto, esta marca convierte un método asincrónico en un método sincrónico.</span><span class="sxs-lookup"><span data-stu-id="57dba-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="57dba-120">El inconveniente es que la interfaz de usuario se bloquea si llama al método desde el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="57dba-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="57dba-121">**Synchronization (objeto)**</span><span class="sxs-lookup"><span data-stu-id="57dba-121">**Synchronization Object**</span></span>

<span data-ttu-id="57dba-122">Todos los métodos asincrónicos pueden devolver un objeto de sincronización, que puede usar para esperar a que el comando se inicie o finalice.</span><span class="sxs-lookup"><span data-stu-id="57dba-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="57dba-123">Para obtener este objeto, pase la dirección de un puntero [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) en el parámetro *ppCmd* :</span><span class="sxs-lookup"><span data-stu-id="57dba-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="57dba-124">Si el método se ejecuta correctamente, devuelve un nuevo objeto **IDvdCmd** .</span><span class="sxs-lookup"><span data-stu-id="57dba-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="57dba-125">El método [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) se bloquea hasta que se inicia el comando y el método [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) se bloquea hasta que finaliza el comando.</span><span class="sxs-lookup"><span data-stu-id="57dba-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="57dba-126">El valor devuelto indica el estado del comando.</span><span class="sxs-lookup"><span data-stu-id="57dba-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="57dba-127">El código siguiente es funcionalmente equivalente a establecer la \_ marca de \_ bloqueo de marca cmd de DVD de EC \_ \_ , que se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57dba-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


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



<span data-ttu-id="57dba-128">En este caso, el método **PlayTitle** no se bloquea, pero la aplicación se bloquea llamando a **WaitForEnd**.</span><span class="sxs-lookup"><span data-stu-id="57dba-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="57dba-129">**Eventos de estado de comando**</span><span class="sxs-lookup"><span data-stu-id="57dba-129">**Command Status Events**</span></span>

<span data-ttu-id="57dba-130">Si establece la \_ \_ \_ marca SendEvents de la marca de cmd de DVD en el parámetro *dwFlags* , el navegador de DVD envía un evento de inicio de cmd de DVD de EC cuando se inicia el comando y un evento de fin de cmd de DVD de EC cuando finaliza el comando. [**\_ \_ \_**](ec-dvd-cmd-start.md) [**\_ \_ \_**](ec-dvd-cmd-end.md)</span><span class="sxs-lookup"><span data-stu-id="57dba-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="57dba-131">El parámetro *lParam2* del evento es el valor devuelto HRESULT para el comando.</span><span class="sxs-lookup"><span data-stu-id="57dba-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="57dba-132">El parámetro *lParam1* del evento proporciona una manera de obtener el objeto de sincronización para el comando.</span><span class="sxs-lookup"><span data-stu-id="57dba-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="57dba-133">Si pasa *lParam1* al método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , el método devuelve un puntero a la interfaz **IDvdCmd** del objeto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="57dba-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="57dba-134">Puede usar esta interfaz para esperar a que finalice el comando, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57dba-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="57dba-135">Sin embargo, si se pasa **null** para el parámetro *ppCmd* en el método **IDvdControl2** original, el explorador de DVD no crea un objeto de sincronización y **GetCmdFromEvent** devuelve \_ un error.</span><span class="sxs-lookup"><span data-stu-id="57dba-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="57dba-136">En el código siguiente se muestra cómo usar eventos de estado de comandos sin ningún objeto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="57dba-136">The following code shows how to use command status events with no synchronization object.</span></span>


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



<span data-ttu-id="57dba-137">Tenga en cuenta que, sin un objeto de sincronización, no se puede saber qué comando está asociado al evento.</span><span class="sxs-lookup"><span data-stu-id="57dba-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="57dba-138">En el código siguiente se muestra cómo utilizar los eventos con el objeto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="57dba-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="57dba-139">La idea es almacenar los objetos de sincronización en una lista y, a continuación, comparar los punteros de objeto cuando se obtiene el evento de [**\_ \_ \_ Inicio**](ec-dvd-cmd-start.md) o el evento de [**\_ \_ \_ fin de CMD**](ec-dvd-cmd-end.md) de DVD de EC.</span><span class="sxs-lookup"><span data-stu-id="57dba-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


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



<span data-ttu-id="57dba-140">**Vaciar los búferes del explorador de DVD**</span><span class="sxs-lookup"><span data-stu-id="57dba-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="57dba-141">Durante la reproducción, el explorador de DVD almacena en búfer los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="57dba-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="57dba-142">La cantidad de datos almacenados en búfer varía.</span><span class="sxs-lookup"><span data-stu-id="57dba-142">The amount of buffered data varies.</span></span> <span data-ttu-id="57dba-143">Cuando el navegador de DVD cambia a un nuevo fragmento de vídeo, los datos que ya están en la canalización no se pierden, por lo que la transición es fluida.</span><span class="sxs-lookup"><span data-stu-id="57dba-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="57dba-144">De forma predeterminada, cuando el navegador de DVD emite un comando, no vacía los datos que ya se encuentren en la canalización.</span><span class="sxs-lookup"><span data-stu-id="57dba-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="57dba-145">Como resultado, puede haber cierta latencia antes de que pueda ver el efecto del comando, en función de la cantidad de datos almacenados en búfer.</span><span class="sxs-lookup"><span data-stu-id="57dba-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="57dba-146">Para aumentar la capacidad de respuesta, puede forzar el vaciado del navegador de DVD si establece la \_ \_ marca de vaciado de marca de cmd de DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="57dba-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="57dba-147">Esta marca se puede combinar con cualquiera de las marcas descritas anteriormente, mediante una operación OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="57dba-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="57dba-148">Un efecto secundario del vaciado es que es posible que se pierda algún vídeo, por lo que no debe usar esta marca si necesita garantizar que no haya espacios en el vídeo.</span><span class="sxs-lookup"><span data-stu-id="57dba-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57dba-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57dba-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57dba-150">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="57dba-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



