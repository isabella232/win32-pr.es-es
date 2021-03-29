---
title: Asegurarse de que Windows Media Player abre el contenido de HTMLView
description: Asegurarse de que Windows Media Player abre el contenido de HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Listas de reproducción de metarchivo de Windows Media, Windows Media Player abrir el contenido de HTMLView
- listas de reproducción, Windows Media Player abrir el contenido de HTMLView
- listas de reproducción de metarchivos, Windows Media Player abrir el contenido de HTMLView
- Listas de reproducción de metarchivos de Windows Media, abrir contenido de HTMLView
- listas de reproducción, abrir contenido de HTMLView
- listas de reproducción de metarchivos, abrir contenido de HTMLView
- abrir el contenido de HTMLView
- Windows Media Player, abrir contenido de HTMLView
- Media Player de Windows, contenido de HTMLView
- HTMLView, abrir contenido
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776512"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="da3c9-113">Asegurarse de que Windows Media Player abre el contenido de HTMLView</span><span class="sxs-lookup"><span data-stu-id="da3c9-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="da3c9-114">Actualmente, las series Windows Media Player 9 y Windows Media Player 10 son los únicos reproductores que admiten el parámetro *HTMLView* en los archivos. ASX.</span><span class="sxs-lookup"><span data-stu-id="da3c9-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="da3c9-115">Esto significa que debe tomar medidas para asegurarse de que el contenido de HTMLView se reproduce en estas versiones de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="da3c9-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="da3c9-116">En primer lugar, debe determinar si Windows Media Player 9 series o Windows Media Player 10 está instalado en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="da3c9-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="da3c9-117">El SDK de Windows Media Player incluye un ejemplo completo que muestra cómo detectar diferentes versiones de Windows Media Player en diferentes exploradores Web.</span><span class="sxs-lookup"><span data-stu-id="da3c9-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="da3c9-118">Aunque un análisis completo del ejemplo de detección está fuera del ámbito de esta sección, hay algunos pasos básicos que puede seguir para determinar qué versión de Windows Media Player el equipo del usuario está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="da3c9-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="da3c9-119">En su forma más sencilla, la detección de Media Player de Windows implica la inserción del control Player en la página web que se vincula al contenido de HTMLView y, a continuación, la inspección del valor recuperado por el *reproductor*. propiedad **versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="da3c9-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="da3c9-120">Una vez que haya comprobado que el usuario tiene Windows Media Player 9 series o Windows Media Player 10 instalado, puede usar el método [Player. openPlayer](player-openplayer.md) para abrir el contenido en el reproductor en modo completo.</span><span class="sxs-lookup"><span data-stu-id="da3c9-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="da3c9-121">El método **openPlayer** garantiza que el contenido se muestra inicialmente en la característica **reproducción en curso** del reproductor en modo completo, en lugar de en una máscara, en el modo de mini reproductor o en otro reproductor que se ha registrado como el programa predeterminado para los archivos con la extensión de nombre de archivo. ASX, pero no es compatible con HTMLView.</span><span class="sxs-lookup"><span data-stu-id="da3c9-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="da3c9-122">Sin embargo, una vez que se muestra el contenido, el usuario tiene el control completo de Windows Media Player, lo que significa que puede elegir mostrar una característica que no sea **reproducción**, cambiar al modo de máscara o incluso salir del reproductor.</span><span class="sxs-lookup"><span data-stu-id="da3c9-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="da3c9-123">En el código de ejemplo siguiente se crea una página web para Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="da3c9-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="da3c9-124">Esta página abre un archivo. ASX, que especifica una página web de HTMLView que aparece en el reproductor de modo completo cuando se instala Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="da3c9-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="da3c9-125">En el código del ejemplo anterior se inserta el control Media Player de Windows con la propiedad **uiMode** establecida en "invisible" y los atributos height y width del reproductor establecidos en cero.</span><span class="sxs-lookup"><span data-stu-id="da3c9-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="da3c9-126">Esto se debe a que la página web no requiere que la interfaz de usuario de control del reproductor se muestre inicialmente, solo requiere acceso al modelo de objetos del reproductor.</span><span class="sxs-lookup"><span data-stu-id="da3c9-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="da3c9-127">La página también muestra un botón de entrada que permite al usuario reproducir el archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="da3c9-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="da3c9-128">Cuando el usuario hace clic en el botón reproducir ASX, se ejecuta la función PlayASX de Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="da3c9-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="da3c9-129">Esta función recupera primero el valor de la propiedad **versionInfo** del reproductor, utilizando el método **parseInt** de JScript para inspeccionar el valor numérico de la cadena recuperada.</span><span class="sxs-lookup"><span data-stu-id="da3c9-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="da3c9-130">Si el valor numérico es mayor o igual que 9 (lo que significa que el usuario tiene instalada la serie Windows Media Player 9), el código de script llama al método **openPlayer** y pasa la dirección URL del archivo. ASX que contiene el parámetro HTMLView.</span><span class="sxs-lookup"><span data-stu-id="da3c9-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="da3c9-131">Este método abre el archivo. ASX con Windows Media Player en modo completo, reproduce el contenido multimedia digital en la lista de reproducción. ASX y muestra el contenido basado en Web HTMLView en la característica de **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="da3c9-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="da3c9-132">Si el valor numérico de la cadena de versión no es mayor o igual que 9 (lo que significa que el usuario no tiene Windows Media Player 9 series o posterior instalado en su equipo), el código de script cambia el **uiMode** del control Player a "Full", establece un nuevo ancho y alto para el control y, a continuación, abre el archivo. asx en el reproductor incrustado especificando un valor para la propiedad **URL** .</span><span class="sxs-lookup"><span data-stu-id="da3c9-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="da3c9-133">Cuando esto sucede, el contenido multimedia digital se reproduce en la página web, pero se omiten los valores de HTMLView especificados en el archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="da3c9-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="da3c9-134">Cómo se reproduce el contenido cuando el usuario no tiene Windows Media Player 9 series o Windows Media Player 10 instalado depende de usted.</span><span class="sxs-lookup"><span data-stu-id="da3c9-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="da3c9-135">En el ejemplo anterior se muestra cómo especificar que el contenido se reproduzca en la página web en lugar de en el reproductor de modo completo, omitiendo el contenido de HTMLView en el proceso.</span><span class="sxs-lookup"><span data-stu-id="da3c9-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="da3c9-136">Hay otros métodos que puede llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="da3c9-136">There are other approaches you might take.</span></span> <span data-ttu-id="da3c9-137">Por ejemplo, puede pedir al usuario que instale una versión más reciente de Windows Media Player, lo que hace que esa versión del reproductor sea un requisito para reproducir el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="da3c9-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da3c9-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da3c9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da3c9-139">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="da3c9-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="da3c9-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="da3c9-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="da3c9-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="da3c9-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




