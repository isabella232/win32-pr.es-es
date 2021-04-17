---
title: Evento Player. comando
description: El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados. | Evento Player. comando
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Media Player comando de eventos de Windows
- Evento comando de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento comando
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709274"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="7d6a0-107">Evento Player. comando</span><span class="sxs-lookup"><span data-stu-id="7d6a0-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="7d6a0-108">El evento **comando** se produce cuando se recibe un comando o una dirección URL sincronizados.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6a0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d6a0-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="7d6a0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d6a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6a0-111">*scType*</span><span class="sxs-lookup"><span data-stu-id="7d6a0-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a0-112">Cadena que especifica el tipo de comando de script.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="7d6a0-113">*Parámetro*</span><span class="sxs-lookup"><span data-stu-id="7d6a0-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a0-114">**Cadena** que especifica el comando de script.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6a0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d6a0-115">Return value</span></span>

<span data-ttu-id="7d6a0-116">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6a0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d6a0-117">Remarks</span></span>

<span data-ttu-id="7d6a0-118">Los comandos se pueden insertar entre los sonidos e imágenes de un archivo o una secuencia de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="7d6a0-119">Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="7d6a0-120">Cuando el flujo alcanza el tiempo asociado con el comando, el control Media Player de Windows envía un evento **comando** con dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="7d6a0-121">Un parámetro especifica el tipo de comando que se va a enviar y el otro parámetro especifica el comando.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="7d6a0-122">El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="7d6a0-123">Cualquier tipo de comando se puede incrustar en un archivo o una secuencia para que lo controle el evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7d6a0-124">En la tabla siguiente se enumeran los tipos de comando de script que Windows Media Player procesa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="7d6a0-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d6a0-125">Type</span></span>                   | <span data-ttu-id="7d6a0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d6a0-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6a0-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="7d6a0-127">CAPTION</span></span>                | <span data-ttu-id="7d6a0-128">El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="7d6a0-129">CESO</span><span class="sxs-lookup"><span data-stu-id="7d6a0-129">EVENT</span></span>                  | <span data-ttu-id="7d6a0-130">Indica al control que ejecute instrucciones definidas para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="7d6a0-131">EXTENSIÓN</span><span class="sxs-lookup"><span data-stu-id="7d6a0-131">FILENAME</span></span>               | <span data-ttu-id="7d6a0-132">El control restablece su propiedad de **dirección URL** , intenta abrir el archivo especificado y comienza a reproducir el nuevo flujo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="7d6a0-133">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="7d6a0-133">OPENEVENT</span></span>              | <span data-ttu-id="7d6a0-134">Almacena en búfer el comando de tipo de evento asociado para la ejecución oportuna del script de eventos.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="7d6a0-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="7d6a0-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="7d6a0-136">El parámetro *param* contiene el texto de letra sincronizado.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="7d6a0-137">Windows Media Player muestra el texto de letra en el área de subtítulos (CC) de la característica de **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="7d6a0-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="7d6a0-138">TEXT</span></span>                   | <span data-ttu-id="7d6a0-139">El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="7d6a0-140">URL</span><span class="sxs-lookup"><span data-stu-id="7d6a0-140">URL</span></span>                    | <span data-ttu-id="7d6a0-141">El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado, si se trata de la *configuración*. la propiedad **invokeURLs** está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="7d6a0-142">Puede incrustar cualquier otro tipo de comando siempre que proporcione código recíproco para controlar el comando.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="7d6a0-143">Aunque el control de Windows Media Player omite los comandos desconocidos, se siguen entregando al evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="7d6a0-144">Los comandos de dirección URL recibidos por el control Media Player de Windows se invocan automáticamente en el explorador Web predeterminado si se trata de la *configuración*. la propiedad **invokeURLs** está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="7d6a0-145">Puede usar la *configuración*. propiedad **defaultFrame** para especificar el marco de destino en el que aparece la Página Web.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="7d6a0-146">La dirección URL enviada a Windows Media Player se procesa con respecto a la dirección URL base especificada en la *configuración*. propiedad **baseurl** .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="7d6a0-147">La dirección URL base se concatena con la dirección URL relativamente especificada, lo que da como resultado una dirección URL totalmente especificada que se pasa como parámetro de comando por el evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7d6a0-148">El control Windows Media Player siempre procesa los comandos de tipo URL de entrada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7d6a0-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="7d6a0-149">Se recibe un comando de tipo URL.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="7d6a0-150">*Configuración*. **baseurl** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="7d6a0-151">Se llama a *comando* .</span><span class="sxs-lookup"><span data-stu-id="7d6a0-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="7d6a0-152">Después de que *comando* devuelve, *configuración*. **invokeURLs** está activada.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="7d6a0-153">Es si se trata de un *valor*. **invokeURLs** es true y el comando es un tipo de dirección URL; se invoca la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="7d6a0-154">Es si se trata de un *valor*. **invokeURLs** es false o si el comando no es un tipo de dirección URL, se omite el comando.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="7d6a0-155">Al crear un archivo de Windows Media, puede especificar el marco en el que se muestra la nueva dirección URL mediante la concatenación de dos símbolos de y comercial y el nombre del marco en el campo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="7d6a0-156">En el ejemplo siguiente se muestran los parámetros de *comando* típicos.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="7d6a0-157">Especifica que se debe iniciar la dirección URL de la *Página* en *el marco frame.*</span><span class="sxs-lookup"><span data-stu-id="7d6a0-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="7d6a0-158">No se llama al evento comando si se está examinando el archivo (reenviado rápido o rápido-invertido).</span><span class="sxs-lookup"><span data-stu-id="7d6a0-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="7d6a0-159">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="7d6a0-160">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6a0-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6a0-161">Requirements</span></span>



| <span data-ttu-id="7d6a0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6a0-162">Requirement</span></span> | <span data-ttu-id="7d6a0-163">Value</span><span class="sxs-lookup"><span data-stu-id="7d6a0-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6a0-164">Versión</span><span class="sxs-lookup"><span data-stu-id="7d6a0-164">Version</span></span><br/> | <span data-ttu-id="7d6a0-165">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7d6a0-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7d6a0-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d6a0-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d6a0-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a0-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6a0-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d6a0-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6a0-169">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="7d6a0-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7d6a0-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7d6a0-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="7d6a0-171">**Settings. baseURL**</span><span class="sxs-lookup"><span data-stu-id="7d6a0-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="7d6a0-172">**Settings. defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="7d6a0-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="7d6a0-173">**Settings. invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="7d6a0-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





