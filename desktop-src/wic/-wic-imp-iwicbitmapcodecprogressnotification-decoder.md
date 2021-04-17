---
description: Implementación de IWICBitmapCodecProgressNotification (descodificador)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementación de IWICBitmapCodecProgressNotification (descodificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716133"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="b0aea-103">Implementación de IWICBitmapCodecProgressNotification (descodificador)</span><span class="sxs-lookup"><span data-stu-id="b0aea-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="b0aea-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0aea-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="b0aea-105">Cuando un códec está realizando una operación de e/s como [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en una imagen grande, puede tardar varios segundos o incluso minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="b0aea-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="b0aea-106">Cuando los usuarios finales no pueden interrumpir una operación de ejecución prolongada, pueden creer que la aplicación se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b0aea-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="b0aea-107">Los usuarios suelen cerrar una aplicación, o incluso reiniciar sus equipos, en un intento de recuperar el control de su equipo cuando una aplicación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="b0aea-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="b0aea-108">Esta interfaz permite a una aplicación especificar una función de devolución de llamada a la que el códec puede llamar a intervalos especificados para notificar al autor de la llamada sobre el progreso de la operación actual.</span><span class="sxs-lookup"><span data-stu-id="b0aea-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="b0aea-109">La aplicación puede usar esta función de devolución de llamada para mostrar una indicación del progreso en la interfaz de usuario para notificar al usuario sobre el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b0aea-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="b0aea-110">Si un usuario hace clic en el botón **Cancelar** del cuadro de diálogo de **progreso** , la aplicación devuelve **WINCODEC \_ Err \_ anulado** de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b0aea-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="b0aea-111">Cuando esto sucede, el códec debe cancelar la operación especificada y volver a propagar este **valor HRESULT** al llamador del método que estaba realizando la operación.</span><span class="sxs-lookup"><span data-stu-id="b0aea-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="b0aea-112">Esta interfaz se debe implementar en la clase descodificador de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="b0aea-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="b0aea-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0aea-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="b0aea-114">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0aea-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="b0aea-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0aea-115">RegisterProgressNotification</span></span>

<span data-ttu-id="b0aea-116">Una aplicación invoca [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) para registrar una función de devolución de llamada a la que el códec puede llamar a intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="b0aea-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="b0aea-117">El primer parámetro, *pfnProgressNotification*, es un puntero a la función de devolución de llamada a la que el códec debe llamar a intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="b0aea-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="b0aea-118">El parámetro *pvData* apunta a algún objeto que el llamador desea que el códec devuelva a la función de devolución de llamada siempre que se invoque la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b0aea-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="b0aea-119">Este objeto puede ser cualquier cosa y no tiene ninguna importancia concreta para el códec.</span><span class="sxs-lookup"><span data-stu-id="b0aea-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="b0aea-120">El parámetro *dwProgressFlags* especifica cuándo el códec debe llamar a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b0aea-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="b0aea-121">Se puede realizar una función o con dos enumeraciones para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="b0aea-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="b0aea-122">La enumeración [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) especifica si se debe llamar a la función de devolución de llamada durante la descodificación (**WICProgressOperationCopyPixels**), la codificación (**WICProgerssOperationWritePixels**) o ambas (**WICProgressOperationAll**).</span><span class="sxs-lookup"><span data-stu-id="b0aea-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="b0aea-123">El códec debe llamar a la función de devolución de llamada a intervalos regulares a lo largo de la operación, pero el autor de la llamada puede especificar determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="b0aea-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="b0aea-124">La enumeración [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica en qué punto de la operación se llamará a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b0aea-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="b0aea-125">Si el autor de la llamada especifica **WICProgressNotificationBegin**, debe llamarlo al principio de la operación (0,0).</span><span class="sxs-lookup"><span data-stu-id="b0aea-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="b0aea-126">Si el autor de la llamada no especifica esto, es opcional.</span><span class="sxs-lookup"><span data-stu-id="b0aea-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="b0aea-127">Del mismo modo, si el autor de la llamada especifica **WICProgerssNotificationEnd**, debe llamarlo cuando se complete la operación (1,0).</span><span class="sxs-lookup"><span data-stu-id="b0aea-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="b0aea-128">Si el autor de la llamada especifica **WICProgressNotificationAll**, debe llamarlo al principio y al final, así como a intervalos regulares durante la operación.</span><span class="sxs-lookup"><span data-stu-id="b0aea-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="b0aea-129">El autor de la llamada también puede especificar **WICProgerssNotificationFrequent**, que indica que desea que se vuelva a llamar a intervalos frecuentes, quizás después de cada par de líneas de recorrido.</span><span class="sxs-lookup"><span data-stu-id="b0aea-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="b0aea-130">(Un llamador normalmente usará esta marca solo para una imagen muy grande). De lo contrario, normalmente debe volver a llamar a intervalos de incrementos de 10 por ciento aproximadamente del número total de líneas de análisis que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="b0aea-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="b0aea-131">Solo se puede registrar una función de devolución de llamada a la vez para un descodificador o una instancia de codificador concretos.</span><span class="sxs-lookup"><span data-stu-id="b0aea-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="b0aea-132">Si una aplicación llama a [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) más de una vez, reemplace la función de devolución de llamada registrada anteriormente por la nueva.</span><span class="sxs-lookup"><span data-stu-id="b0aea-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="b0aea-133">Para cancelar un registro de devolución de llamada, un llamador establecerá el parámetro *pfnProgressNotification* en **null**.</span><span class="sxs-lookup"><span data-stu-id="b0aea-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="b0aea-134">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0aea-134">PFNProgressNotification</span></span>

<span data-ttu-id="b0aea-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) es la función de devolución de llamada con la firma siguiente.</span><span class="sxs-lookup"><span data-stu-id="b0aea-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="b0aea-136">Al invocar la función de devolución de llamada, use el parámetro *pvData* para devolver el mismo *pvData* que la aplicación especificó cuando registró la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b0aea-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="b0aea-137">El parámetro *uFrameNum* debe indicar el índice del marco que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="b0aea-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="b0aea-138">Establezca el parámetro Operation en **WICProgressOperationCopyPixels** al descodificar y **WICProgressOperationWritePixels** al codificar.</span><span class="sxs-lookup"><span data-stu-id="b0aea-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="b0aea-139">El parámetro *dblProgress* debe ser un número entre 0,0 (el inicio de la operación) y 1,0 (la finalización de la operación).</span><span class="sxs-lookup"><span data-stu-id="b0aea-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="b0aea-140">El valor debe reflejar la proporción de líneas de recorrido ya procesadas en relación con el número total de líneas de análisis que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="b0aea-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0aea-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0aea-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0aea-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b0aea-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0aea-143">**ProgressNotificationCallback**</span><span class="sxs-lookup"><span data-stu-id="b0aea-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="b0aea-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="b0aea-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="b0aea-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b0aea-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0aea-146">Implementar IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="b0aea-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="b0aea-147">Implementación de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="b0aea-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="b0aea-148">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b0aea-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b0aea-149">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="b0aea-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



