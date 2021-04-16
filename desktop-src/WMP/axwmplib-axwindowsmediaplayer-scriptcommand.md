---
title: Evento comando del objeto AxWindowsMediaPlayer
description: El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados. | Evento comando del objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento comando del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699706"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="59cac-105">Evento comando del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="59cac-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="59cac-106">El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados.</span><span class="sxs-lookup"><span data-stu-id="59cac-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="59cac-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="59cac-107">Event Data</span></span>

<span data-ttu-id="59cac-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="59cac-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="59cac-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="59cac-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="59cac-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59cac-110">Property</span></span> | <span data-ttu-id="59cac-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="59cac-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="59cac-112">scType</span><span class="sxs-lookup"><span data-stu-id="59cac-112">scType</span></span>   | <span data-ttu-id="59cac-113">System. StringSpecifies el tipo de comando de script.</span><span class="sxs-lookup"><span data-stu-id="59cac-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="59cac-114">param</span><span class="sxs-lookup"><span data-stu-id="59cac-114">param</span></span>    | <span data-ttu-id="59cac-115">System. StringSpecifies el comando de script.</span><span class="sxs-lookup"><span data-stu-id="59cac-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="59cac-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59cac-116">Remarks</span></span>

<span data-ttu-id="59cac-117">Los comandos se pueden insertar entre los sonidos e imágenes de un archivo o una secuencia de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="59cac-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="59cac-118">Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="59cac-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="59cac-119">Cuando el flujo alcanza el tiempo asociado con el comando, el control Media Player de Windows envía un evento **comando** con dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="59cac-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="59cac-120">Un parámetro especifica el tipo de comando que se va a enviar y el otro parámetro especifica el comando.</span><span class="sxs-lookup"><span data-stu-id="59cac-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="59cac-121">El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="59cac-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="59cac-122">Cualquier tipo de comando se puede incrustar en un archivo o una secuencia para que lo controle el evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="59cac-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="59cac-123">En la tabla siguiente se enumeran los tipos de comando de script que Windows Media Player procesa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="59cac-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="59cac-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="59cac-124">Type</span></span>                   | <span data-ttu-id="59cac-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="59cac-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cac-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="59cac-126">CAPTION</span></span>                | <span data-ttu-id="59cac-127">El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="59cac-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="59cac-128">CESO</span><span class="sxs-lookup"><span data-stu-id="59cac-128">EVENT</span></span>                  | <span data-ttu-id="59cac-129">El control ejecuta instrucciones definidas para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="59cac-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="59cac-130">EXTENSIÓN</span><span class="sxs-lookup"><span data-stu-id="59cac-130">FILENAME</span></span>               | <span data-ttu-id="59cac-131">El control restablece su propiedad de **dirección URL** , intenta abrir el archivo especificado y comienza a reproducir el nuevo flujo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="59cac-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="59cac-132">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="59cac-132">OPENEVENT</span></span>              | <span data-ttu-id="59cac-133">Almacena en búfer el comando de tipo de evento asociado para la ejecución oportuna del script de eventos.</span><span class="sxs-lookup"><span data-stu-id="59cac-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="59cac-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="59cac-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="59cac-135">El parámetro *param* contiene el texto de letra sincronizado.</span><span class="sxs-lookup"><span data-stu-id="59cac-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="59cac-136">Windows Media Player muestra el texto de letra en el área de subtítulos (CC) de la característica de **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="59cac-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="59cac-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="59cac-137">TEXT</span></span>                   | <span data-ttu-id="59cac-138">El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="59cac-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="59cac-139">URL</span><span class="sxs-lookup"><span data-stu-id="59cac-139">URL</span></span>                    | <span data-ttu-id="59cac-140">El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado si IWMPSettings. la propiedad **invokeURLs** está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="59cac-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="59cac-141">Puede incrustar cualquier otro tipo de comando siempre que proporcione código para controlar el comando.</span><span class="sxs-lookup"><span data-stu-id="59cac-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="59cac-142">Aunque el control de Windows Media Player omite los comandos desconocidos, se siguen entregando al evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="59cac-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="59cac-143">No se llama al evento comando si el archivo se está examinando en modo de avance rápido o de rebobinado.</span><span class="sxs-lookup"><span data-stu-id="59cac-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="59cac-144">Los comandos de dirección URL recibidos por el control Media Player de Windows se invocan automáticamente en el explorador Web predeterminado si IWMPSettings. la propiedad **invokeURLs** está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="59cac-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="59cac-145">Puede usar IWMPSettings. propiedad **defaultFrame** para especificar el marco de destino en el que aparece la Página Web.</span><span class="sxs-lookup"><span data-stu-id="59cac-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="59cac-146">La dirección URL enviada a Windows Media Player se procesa con respecto a la dirección URL base especificada por IWMPSettings. propiedad **baseurl** .</span><span class="sxs-lookup"><span data-stu-id="59cac-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="59cac-147">La dirección URL base se concatena con la dirección URL relativa, lo que da como resultado una dirección URL completa que se pasa como parámetro de comando por el evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="59cac-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="59cac-148">El control de Windows Media Player siempre procesa los comandos de dirección URL de entrada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="59cac-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="59cac-149">Se recibe un comando de tipo URL.</span><span class="sxs-lookup"><span data-stu-id="59cac-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="59cac-150">IWMPSettings. **baseurl** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.</span><span class="sxs-lookup"><span data-stu-id="59cac-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="59cac-151">Se llama a **comando** .</span><span class="sxs-lookup"><span data-stu-id="59cac-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="59cac-152">Después de que **comando** devuelve, IWMPSettings. **invokeURLs** está activada.</span><span class="sxs-lookup"><span data-stu-id="59cac-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="59cac-153">Si IWMPSettings. **invokeURLs** es true y el comando es un comando de dirección URL, se invoca la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="59cac-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="59cac-154">Si IWMPSettings. **invokeURLs** es false o si el comando no es un comando de dirección URL, se omite el comando.</span><span class="sxs-lookup"><span data-stu-id="59cac-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="59cac-155">Al crear un archivo de Windows Media, puede especificar el marco en el que se muestra la nueva dirección URL mediante la concatenación de dos símbolos de y comercial y el nombre del marco en el campo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="59cac-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="59cac-156">En el ejemplo siguiente se muestran los parámetros de **comando** típicos.</span><span class="sxs-lookup"><span data-stu-id="59cac-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="59cac-157">Especifica que se debe iniciar la dirección URL de la *Página* en *el marco frame.*</span><span class="sxs-lookup"><span data-stu-id="59cac-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="59cac-158">No se llama al evento comando si se está examinando el archivo (reenvío rápido o rebobinado).</span><span class="sxs-lookup"><span data-stu-id="59cac-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="59cac-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59cac-159">Requirements</span></span>



| <span data-ttu-id="59cac-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cac-160">Requirement</span></span> | <span data-ttu-id="59cac-161">Value</span><span class="sxs-lookup"><span data-stu-id="59cac-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cac-162">Versión</span><span class="sxs-lookup"><span data-stu-id="59cac-162">Version</span></span><br/>   | <span data-ttu-id="59cac-163">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="59cac-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="59cac-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59cac-164">Namespace</span></span><br/> | <span data-ttu-id="59cac-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="59cac-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="59cac-166">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="59cac-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="59cac-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="59cac-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59cac-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="59cac-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cac-169">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59cac-170">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59cac-171">**IWMPClosedCaption. captioningId (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59cac-172">**IWMPSettings. baseURL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59cac-173">**IWMPSettings. defaultFrame (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59cac-174">**IWMPSettings. invokeURLs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="59cac-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





