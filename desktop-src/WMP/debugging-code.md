---
title: Depurar código
description: Depurar código
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Aspectos de Windows Media Player, código de depuración
- máscaras, código de depuración
- depurar código para máscaras
- Máscaras de Windows Media Player, registro
- máscaras, registro
- funcionalidad de registro en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357611"
---
# <a name="debugging-code"></a><span data-ttu-id="e388a-109">Depurar código</span><span class="sxs-lookup"><span data-stu-id="e388a-109">Debugging Code</span></span>

<span data-ttu-id="e388a-110">A menudo, querrá ver lo que está ocurriendo dentro de la máscara.</span><span class="sxs-lookup"><span data-stu-id="e388a-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="e388a-111">Puede hacerlo a través de un control de texto o de un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="e388a-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="e388a-112">Puede crear un elemento de **texto** y colocarlo en una parte de la máscara temporalmente.</span><span class="sxs-lookup"><span data-stu-id="e388a-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="e388a-113">Por ejemplo, podría usar el código siguiente para crear el elemento de **texto** :</span><span class="sxs-lookup"><span data-stu-id="e388a-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="e388a-114">Después, por ejemplo, si desea ver la posición actual del contenido multimedia digital en Windows Media Player, puede usar código similar al siguiente para mostrar la posición actual en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="e388a-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="e388a-115">Para escribir información de depuración en un archivo de registro</span><span class="sxs-lookup"><span data-stu-id="e388a-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="e388a-116">Para habilitar o deshabilitar la depuración, cambie el valor de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="e388a-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="e388a-117">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**</span><span class="sxs-lookup"><span data-stu-id="e388a-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="e388a-118">Al establecer el valor en 1, el registro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e388a-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="e388a-119">Al establecer el valor en 0 (el valor predeterminado), el registro está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e388a-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="e388a-120">Si el registro está habilitado, se colocará un archivo en el equipo del usuario en la misma carpeta que la máscara.</span><span class="sxs-lookup"><span data-stu-id="e388a-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="e388a-121">El archivo se denominará "*filename* \_ 0 \_log.txt", donde *filename* es el nombre del archivo de máscara.</span><span class="sxs-lookup"><span data-stu-id="e388a-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="e388a-122">El código de la máscara puede escribir texto en este archivo mediante el *tema*. método **logString** .</span><span class="sxs-lookup"><span data-stu-id="e388a-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="e388a-123">Esto puede ser útil si desea determinar lo que está ocurriendo dentro del código mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e388a-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="e388a-124">Tenga en cuenta que el archivo de texto se codifica con caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="e388a-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="e388a-125">Cuando el registro está habilitado y se ha instalado un sistema de desarrollo que proporciona capacidades de depuración (como Microsoft Visual Studio), las excepciones que no se controlan mediante el código de script provocarán que se abra un cuadro de diálogo de advertencia del depurador para cada excepción.</span><span class="sxs-lookup"><span data-stu-id="e388a-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="e388a-126">Esta es una característica útil para ayudarle a depurar el código de script.</span><span class="sxs-lookup"><span data-stu-id="e388a-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="e388a-127">Además, puede adjuntar manualmente el proceso de Media Player de Windows al depurador cuando el registro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e388a-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="e388a-128">Este SDK incluye una máscara de ejemplo, denominada "Logging", que muestra la funcionalidad de registro en máscaras.</span><span class="sxs-lookup"><span data-stu-id="e388a-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="e388a-129">Para obtener más información sobre el uso de los ejemplos, vea [ejemplos](samples.md).</span><span class="sxs-lookup"><span data-stu-id="e388a-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e388a-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e388a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e388a-131">**Acerca de las máscaras**</span><span class="sxs-lookup"><span data-stu-id="e388a-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




