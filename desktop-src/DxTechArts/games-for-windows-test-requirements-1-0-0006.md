---
title: 'Casos de prueba de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan casos de prueba para juegos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078076"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="feb39-103">Juegos para casos de prueba de Windows: prácticas recomendadas para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8</span><span class="sxs-lookup"><span data-stu-id="feb39-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="feb39-104">En este artículo se proporcionan casos de prueba para juegos para Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="feb39-105">Cómo usar este artículo</span><span class="sxs-lookup"><span data-stu-id="feb39-105">How to Use This Article</span></span>

<span data-ttu-id="feb39-106">Hay tres secciones principales en este artículo:</span><span class="sxs-lookup"><span data-stu-id="feb39-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="feb39-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de pruebas**</span><span class="sxs-lookup"><span data-stu-id="feb39-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="feb39-108">Cada requisito de prueba de este documento tiene cuatro secciones principales: un título y una tabla con tres secciones destacadas (columna izquierda, superior derecha, inferior derecha).</span><span class="sxs-lookup"><span data-stu-id="feb39-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="feb39-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titulo</span><span class="sxs-lookup"><span data-stu-id="feb39-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="feb39-110">Nombre del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="feb39-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Cuadro, columna izquierda</span><span class="sxs-lookup"><span data-stu-id="feb39-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="feb39-112">Nombres de los sistemas operativos a los que se aplica el caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="feb39-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Cuadro, parte superior derecha</span><span class="sxs-lookup"><span data-stu-id="feb39-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="feb39-114">Breve resumen del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="feb39-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Cuadro, parte inferior derecha</span><span class="sxs-lookup"><span data-stu-id="feb39-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="feb39-116">Detalles del caso de prueba real.</span><span class="sxs-lookup"><span data-stu-id="feb39-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="feb39-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script de prueba de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="feb39-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="feb39-118">Esta sección es un ejemplo de la secuencia que seguiría un paso de prueba típico si usara los requisitos de prueba como guía.</span><span class="sxs-lookup"><span data-stu-id="feb39-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="feb39-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas de la herramienta de prueba**</span><span class="sxs-lookup"><span data-stu-id="feb39-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="feb39-120">Esta sección contiene notas detalladas sobre cada una de las herramientas de prueba que se usan para comprobar las condiciones superadas o erróneas en los requisitos de pruebas.</span><span class="sxs-lookup"><span data-stu-id="feb39-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="feb39-121">Requisitos de pruebas</span><span class="sxs-lookup"><span data-stu-id="feb39-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="feb39-122">1. requisitos del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="feb39-123">Explorador de juegos de Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="feb39-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-124">Windows 7</span></span><br/> <span data-ttu-id="feb39-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-126">El juego debe estar visible en el explorador de juegos de Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb39-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="feb39-127">Cuando se selecciona, el juego también debe mostrar los metadatos correctos.</span><span class="sxs-lookup"><span data-stu-id="feb39-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="feb39-128">La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="feb39-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="feb39-129">No se deben crear tareas ni accesos directos para quitarlos.</span><span class="sxs-lookup"><span data-stu-id="feb39-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-130">Después de instalar el juego, abra el explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="feb39-131">Compruebe que el icono de juego se muestra en el explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="feb39-132">Haga clic con el botón secundario en el icono y pruebe cada tarea de soporte & de reproducción definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="feb39-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="feb39-133">Haga clic en el icono y compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) de la parte inferior se muestran y son correctos.</span><span class="sxs-lookup"><span data-stu-id="feb39-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="feb39-134">Compruebe que el icono de juego muestra información del índice de experiencia de Windows (WEI) en el explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="feb39-135">Compruebe que los hipervínculos de juego para metadatos funcionan correctamente en el explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="feb39-136">(Si no se muestran los hipervínculos, es posible que el archivo exe no esté firmado; vea la <a href="#23-sign-files">sección 2,3</a>).</span><span class="sxs-lookup"><span data-stu-id="feb39-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="feb39-137">Compruebe que el juego muestra la clasificación de control parental exacta en el explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="feb39-138">(Si dice sin clasificación, compruebe que se trata de un juego sin clasificación; de lo contrario, es un indicador de que el archivo exe no está firmado; vea la <a href="#23-sign-files">sección 2,3</a>).</span><span class="sxs-lookup"><span data-stu-id="feb39-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="feb39-139">Compruebe que el juego no coloca accesos directos de inicio en el escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="feb39-140">Haga clic en Inicio-> todos los programas.</span><span class="sxs-lookup"><span data-stu-id="feb39-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="feb39-141">Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="feb39-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="feb39-142">Compruebe que el juego no coloca los accesos directos de desinstalación en el menú Inicio fuera del panel de control.</span><span class="sxs-lookup"><span data-stu-id="feb39-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="feb39-143">Si el juego está distribuido digitalmente, compruebe que el proveedor de servicios aparece en el explorador de juegos de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="feb39-144">1,2 protección de la familia de Windows/control parental</span><span class="sxs-lookup"><span data-stu-id="feb39-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-145">Windows 7</span></span><br/> <span data-ttu-id="feb39-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-147">El juego debe ejecutarse en el contexto de un &quot; usuario estándar &quot; .</span><span class="sxs-lookup"><span data-stu-id="feb39-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="feb39-148">Los controles parentales deben ser capaces de bloquear el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="feb39-149">Compruebe que GDF tiene nombres de EXE.</span><span class="sxs-lookup"><span data-stu-id="feb39-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-150">Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="feb39-151">Inicio > panel de control-> agregar o quitar cuentas de usuario-> crear una cuenta nueva</span><span class="sxs-lookup"><span data-stu-id="feb39-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="feb39-152">Como Julia, desde la cuenta de administrador configura controles parentales para el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="feb39-153">Inicio-> panel de control-> configurar controles parentales para cualquier usuario > Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="feb39-154">Compruebe que el juego se inicia desde el icono del explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="feb39-155">Compruebe que el juego muestra la clasificación de control parental exacta debajo del título del juego en el panel de control de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="feb39-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="feb39-156">Antes de aplicar controles parentales, compruebe que el juego no solicita credenciales de administrador al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="feb39-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="feb39-157">Establezca controles parentales en &quot; activado &quot; .</span><span class="sxs-lookup"><span data-stu-id="feb39-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="feb39-158">En la sección configuración de Windows, haga clic en juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="feb39-159">Haga clic en Aceptar (el valor debe ser ahora &quot; AO/todos los juegos &quot; ).</span><span class="sxs-lookup"><span data-stu-id="feb39-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="feb39-160">Compruebe que el juego se ejecuta con esta configuración como User Jane.</span><span class="sxs-lookup"><span data-stu-id="feb39-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="feb39-161">Cierre la sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="feb39-162">Compruebe que el juego se ejecuta con esta configuración como User Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="feb39-163">Cierre la sesión como Toby e inicie sesión como Julia.</span><span class="sxs-lookup"><span data-stu-id="feb39-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="feb39-164">Vuelva a la pantalla anterior y seleccione &quot; establecer clasificaciones de &quot; juegos.</span><span class="sxs-lookup"><span data-stu-id="feb39-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="feb39-165">Seleccione una clasificación inferior a la clasificación de ESRB del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-166">Si el juego no está clasificado, omita este paso y vaya a la siguiente parte de esta prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="feb39-167">Puede que sea necesario elegir otro sistema de clasificación para encontrar una clasificación de juego, en función de la configuración regional de idioma de la SKU que se está probando.</span><span class="sxs-lookup"><span data-stu-id="feb39-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="feb39-168">Cierre la sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="feb39-169">Compruebe que el juego no se inicia para el usuario Toby cuando ESRB está bloqueado por el usuario Jane.</span><span class="sxs-lookup"><span data-stu-id="feb39-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="feb39-170">Cierre la sesión como Toby e inicie sesión como Julia.</span><span class="sxs-lookup"><span data-stu-id="feb39-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="feb39-171">Si ha cambiado previamente, restaure la configuración de ESRB.</span><span class="sxs-lookup"><span data-stu-id="feb39-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="feb39-172">Si no hay ninguna configuración de ESRB, seleccione &quot; bloquear o permitir juegos específicos &quot; y seleccione el juego por nombre.</span><span class="sxs-lookup"><span data-stu-id="feb39-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="feb39-173">Cierre la sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="feb39-174">Compruebe que el juego no se inicia para el usuario Toby cuando el usuario Julia bloquea el archivo EXE/Name.</span><span class="sxs-lookup"><span data-stu-id="feb39-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="feb39-175">Cierre la sesión como Toby y vuelva a iniciarla como Julia.</span><span class="sxs-lookup"><span data-stu-id="feb39-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="feb39-176">Como Julia, abra controles de usuario-> restricciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="feb39-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="feb39-177">Haga clic en &quot; Toby solo puede usar los programas que se permiten &quot; y hacer clic en Aceptar (es decir, no permitir ningún exe).</span><span class="sxs-lookup"><span data-stu-id="feb39-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="feb39-178">Vaya a controles de usuario | Controla los juegos y permite el juego específico con la Clasificación ESRB.</span><span class="sxs-lookup"><span data-stu-id="feb39-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="feb39-179">Cierre la sesión como Julia e inicie sesión como Toby e intente jugar al juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="feb39-180">Compruebe que el juego no está bloqueado y que Toby puede reproducirlo cuando &quot; no &quot; se ha establecido permitir ningún exe.</span><span class="sxs-lookup"><span data-stu-id="feb39-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="feb39-181">1,3 juegos guardados enriquecidos de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="feb39-182">Este requisito se ha retirado.</span><span class="sxs-lookup"><span data-stu-id="feb39-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="feb39-183">1,4 Xbox 360 Common Controller for Windows \[ requisito condicional\]</span><span class="sxs-lookup"><span data-stu-id="feb39-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-184">Windows 7</span></span><br/> <span data-ttu-id="feb39-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-185">Windows Vista</span></span><br/> <span data-ttu-id="feb39-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-187">Los juegos que admiten controladores de controlador para juegos deben admitir la controladora Xbox 360 para Windows mediante la API de XInput.</span><span class="sxs-lookup"><span data-stu-id="feb39-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="feb39-188">Todas las referencias a los botones y desencadenadores de controlador comunes deben usar los nombres de Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="feb39-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-189">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-189">Launch the game.</span></span></li>
<li><span data-ttu-id="feb39-190">Vaya a las opciones del controlador.</span><span class="sxs-lookup"><span data-stu-id="feb39-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="feb39-191">Compruebe que el juego reconoce el controlador Xbox 360 para Windows como dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="feb39-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="feb39-192">Juega el juego y comprueba que el juego y el sistema de menús se pueden controlar con el controlador Xbox 360 para Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="feb39-193">Compruebe que la controladora Xbox 360 para Windows se comporta de acuerdo con los estándares aceptados.</span><span class="sxs-lookup"><span data-stu-id="feb39-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="feb39-194">(B para atrás, para aceptar, iniciar para en el menú juego/pausar o aceptar, etc.)</span><span class="sxs-lookup"><span data-stu-id="feb39-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="feb39-195">Compruebe que el juego hace referencia a los botones del controlador y a los desencadenadores mediante los nombres de Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="feb39-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-196">Si el juego no es compatible con un dispositivo de juego o solo es compatible con el teclado o el mouse, omita este caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="feb39-197">\* \* La configuración del controlador podría encontrarse fuera del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="feb39-198">1,5 varias relaciones y resoluciones de aspecto</span><span class="sxs-lookup"><span data-stu-id="feb39-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-199">Windows 7</span></span><br/> <span data-ttu-id="feb39-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-200">Windows Vista</span></span><br/> <span data-ttu-id="feb39-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-202">El juego debe admitir al menos las siguientes proporciones de aspecto y las resoluciones de pantalla asociadas:</span><span class="sxs-lookup"><span data-stu-id="feb39-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="feb39-203">4:3 &quot; normal &quot; (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="feb39-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="feb39-204">&quot;pantalla panorámica 16:9 &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="feb39-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="feb39-205">16:10 &quot; pantalla panorámica &quot; (1152 720, 1680 1050 o 800 480)</span><span class="sxs-lookup"><span data-stu-id="feb39-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-206">Busque las opciones de vídeo del juego (esto puede estar fuera del juego).</span><span class="sxs-lookup"><span data-stu-id="feb39-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-207">Las siguientes pruebas deben realizarse en un monitor de pantalla panorámica.</span><span class="sxs-lookup"><span data-stu-id="feb39-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="feb39-208">En la sección resolución de vídeo, seleccione 800 600 o 1024 768.</span><span class="sxs-lookup"><span data-stu-id="feb39-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="feb39-209">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 4:3.</span><span class="sxs-lookup"><span data-stu-id="feb39-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="feb39-210">En la sección resolución de vídeo, seleccione 1280 720.</span><span class="sxs-lookup"><span data-stu-id="feb39-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="feb39-211">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9.</span><span class="sxs-lookup"><span data-stu-id="feb39-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="feb39-212">En la sección resolución de vídeo, seleccione 1680 1050, 800 480 o 1152 720.</span><span class="sxs-lookup"><span data-stu-id="feb39-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="feb39-213">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:10.</span><span class="sxs-lookup"><span data-stu-id="feb39-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="feb39-214">Compruebe que el juego no estire la imagen y, a su vez, presente un área más amplia de la vista.</span><span class="sxs-lookup"><span data-stu-id="feb39-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="feb39-215">Compruebe que el juego solicita al usuario cuando se realiza un cambio en la resolución.</span><span class="sxs-lookup"><span data-stu-id="feb39-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="feb39-216">Si el usuario no acepta en 15 segundos, compruebe que la pantalla revierte a la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="feb39-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="feb39-217">Compruebe que el juego no agrega barras negras a la izquierda y a la derecha del área de juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="feb39-218">(En este caso, verá que el área de juego sigue teniendo una relación 4:3 en el centro de la pantalla).</span><span class="sxs-lookup"><span data-stu-id="feb39-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="feb39-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="feb39-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="feb39-220">Este requisito se ha retirado.</span><span class="sxs-lookup"><span data-stu-id="feb39-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="feb39-221">1,7 \[ requisito condicional de Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="feb39-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb39-222">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-222">Windows 7</span></span><br/> <span data-ttu-id="feb39-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-223">Windows Vista</span></span><br/> <span data-ttu-id="feb39-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-224">Windows XP</span></span><br/> | <span data-ttu-id="feb39-225">Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el valor predeterminado de cualquier opción de configuración de pantalla.</span><span class="sxs-lookup"><span data-stu-id="feb39-225">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <span data-ttu-id="feb39-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span><span class="sxs-lookup"><span data-stu-id="feb39-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="feb39-227">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-227">Launch the game.</span></span> <span data-ttu-id="feb39-228">En las opciones de vídeo, compruebe si hay opciones de representación, D3D y/o OpenGL.</span><span class="sxs-lookup"><span data-stu-id="feb39-228">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="feb39-229">Si es así, compruebe que las opciones de representación de juego tienen como valor predeterminado Direct3D.</span><span class="sxs-lookup"><span data-stu-id="feb39-229">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="feb39-230">Si no puede comprobar que D3D9 es la versión de DirectX que se está usando, continúe con la prueba automatizada.</span><span class="sxs-lookup"><span data-stu-id="feb39-230">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="feb39-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt></span><span class="sxs-lookup"><span data-stu-id="feb39-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="feb39-232">Herramienta de uso: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-232">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="feb39-233">1,8 habilitar reconocimiento de PPP alto</span><span class="sxs-lookup"><span data-stu-id="feb39-233">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-234">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-234">Windows 7</span></span><br/> <span data-ttu-id="feb39-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-235">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-236">Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando está habilitado el escalado de PPP.</span><span class="sxs-lookup"><span data-stu-id="feb39-236">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="feb39-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="feb39-238">Establezca el sistema en PPP 150%:</span><span class="sxs-lookup"><span data-stu-id="feb39-238">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="feb39-239">Windows Vista: panel de control: personalización, ajustar tamaño de fuente (PPP), PPP personalizado.</span><span class="sxs-lookup"><span data-stu-id="feb39-239">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="feb39-240">Establézcalo en 150%.</span><span class="sxs-lookup"><span data-stu-id="feb39-240">Set to 150%.</span></span><br/> <span data-ttu-id="feb39-241">Windows 7: panel de control: mostrar, establecer en un valor mayor que 150%.</span><span class="sxs-lookup"><span data-stu-id="feb39-241">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="feb39-242">Ejecute el proceso de instalación y el juego para comprobar que no hay problemas con pantallas o cuadros de diálogo recortados.</span><span class="sxs-lookup"><span data-stu-id="feb39-242">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="feb39-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="feb39-244">Compruebe que el elemento <dpiAware>true</dpiAware> está incluido en el manifiesto incrustado.</span><span class="sxs-lookup"><span data-stu-id="feb39-244">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="feb39-245">Herramienta de uso: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-245">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="feb39-246">2. seguridad y compatibilidad</span><span class="sxs-lookup"><span data-stu-id="feb39-246">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="feb39-247">2,1 Siga las directrices de control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="feb39-247">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-248">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-248">Windows 7</span></span><br/> <span data-ttu-id="feb39-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-249">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-250">Todos los archivos ejecutables (. La extensión EXE) que se incluye con una aplicación debe tener un manifiesto incrustado que defina su nivel de ejecución:</span><span class="sxs-lookup"><span data-stu-id="feb39-250">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-251">En el caso de los juegos y los instaladores de juegos, uiAccess siempre debe establecerse en &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="feb39-251">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-252">Compruebe que los archivos ejecutables del juego contienen manifiestos.</span><span class="sxs-lookup"><span data-stu-id="feb39-252">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="feb39-253">Compruebe que el archivo ejecutable del juego requestedExecutionLevel es &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="feb39-253">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="feb39-254">Herramienta de uso: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-254">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="feb39-255">2,2 compatibilidad con versiones x64 de Windows</span><span class="sxs-lookup"><span data-stu-id="feb39-255">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-256">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-256">Windows 7</span></span><br/> <span data-ttu-id="feb39-257">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-257">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-258">Para mantener la compatibilidad con las versiones x64 de Windows:</span><span class="sxs-lookup"><span data-stu-id="feb39-258">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="feb39-259">Los instaladores de títulos y títulos no deben contener código de 16 bits ni confiar en ningún componente de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="feb39-259">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="feb39-260">Si el juego depende de los controladores en modo kernel para su funcionamiento, las versiones x64 de estos controladores deben estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="feb39-260">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="feb39-261">La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-261">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-262">La compatibilidad con la edición de 64 bits de Windows XP Professional es opcional.</span><span class="sxs-lookup"><span data-stu-id="feb39-262">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-263">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="feb39-263">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-264">Ejecute el juego en las ediciones de 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-264">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="feb39-265">Compruebe que el proceso de instalación del juego se ejecuta normalmente en las ediciones de 64 bits de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb39-265">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="feb39-266">Compruebe que el juego no encuentra un error como resultado de los ejecutables de 16 bits en las ediciones de 64 bits de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb39-266">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="feb39-267">El error hará mención a la aplicación de 16 bits en la ventana de error.</span><span class="sxs-lookup"><span data-stu-id="feb39-267">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="feb39-268">Si el juego tiene un archivo ejecutable nativo de 64 bits, úselo también.</span><span class="sxs-lookup"><span data-stu-id="feb39-268">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="feb39-269">Archivos de firma de 2,3</span><span class="sxs-lookup"><span data-stu-id="feb39-269">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-270">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-270">Windows 7</span></span><br/> <span data-ttu-id="feb39-271">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-271">Windows Vista</span></span><br/> <span data-ttu-id="feb39-272">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-272">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-273">Todos los archivos de código ejecutable (por ejemplo, las extensiones. exe y. dll) deben estar firmados con un certificado Authenticode.</span><span class="sxs-lookup"><span data-stu-id="feb39-273">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="feb39-274">Si está utilizando Windows Installer, los archivos de paquete del instalador (archivos. msi) deben estar firmados.</span><span class="sxs-lookup"><span data-stu-id="feb39-274">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-275">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="feb39-275">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-276">Navegue hasta el directorio del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-276">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="feb39-277">Busque todos los archivos. exe y. dll.</span><span class="sxs-lookup"><span data-stu-id="feb39-277">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="feb39-278">Haga clic con el botón secundario en propiedades en cada archivo.</span><span class="sxs-lookup"><span data-stu-id="feb39-278">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="feb39-279">Compruebe que los archivos ejecutables del juego contienen una firma digital.</span><span class="sxs-lookup"><span data-stu-id="feb39-279">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="feb39-280">Controladores de firma de 2,4</span><span class="sxs-lookup"><span data-stu-id="feb39-280">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-281">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-281">Windows 7</span></span><br/> <span data-ttu-id="feb39-282">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-282">Windows Vista</span></span><br/> <span data-ttu-id="feb39-283">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-283">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-284">Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-284">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="feb39-285">Cualquier controlador de dispositivo de hardware en modo de kernel instalado por el juego debe tener una firma de Microsoft obtenida a través del programa de calidad de hardware de Windows (WHQL) o la firma de confiabilidad de controlador (DRS).</span><span class="sxs-lookup"><span data-stu-id="feb39-285">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-286">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="feb39-286">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-287">Instale el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-287">Install the game.</span></span></li>
<li><span data-ttu-id="feb39-288">Compruebe que el proceso de instalación del juego no muestra cuadros de diálogo de controladores sin firmar.</span><span class="sxs-lookup"><span data-stu-id="feb39-288">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="feb39-289">2,5 realizar la comprobación de versiones correctamente</span><span class="sxs-lookup"><span data-stu-id="feb39-289">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-290">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-290">Windows 7</span></span><br/> <span data-ttu-id="feb39-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-291">Windows Vista</span></span><br/> <span data-ttu-id="feb39-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-292">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-293">Los juegos no deben ejecutarse en sistemas operativos futuros, tal como se indica en los cambios en el número de versión de Windows, a menos que el contrato de licencia para el usuario final prohíba su uso en sistemas operativos futuros.</span><span class="sxs-lookup"><span data-stu-id="feb39-293">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="feb39-294">Si se supone que el juego produce un error, debe hacerlo correctamente mostrando un mensaje al usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-294">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="feb39-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="feb39-296">Instale el juego en Windows XP, en las ediciones de 32 bits de Windows Vista y Windows 7, y en las ediciones de 64 bits de Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb39-296">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="feb39-297">Compruebe que el proceso de instalación del juego no encuentra un error relacionado con la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="feb39-297">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="feb39-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="feb39-299">Herramienta de uso: comprobador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="feb39-299">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-300">Inicie comprobador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="feb39-300">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="feb39-301">Habilite la prueba Compatibility: HighVersionLie después de seleccionar el INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="feb39-301">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="feb39-302">Instale el juego y asegúrese de que no bloquee la instalación en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="feb39-302">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="feb39-303">Habilite la prueba Compatibility: HighVersionLie después de seleccionar el GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="feb39-303">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="feb39-304">Ejecute el juego y asegúrese de que no bloquee la ejecución en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="feb39-304">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="feb39-305">2,6 compatibilidad con sesiones de usuario simultáneas</span><span class="sxs-lookup"><span data-stu-id="feb39-305">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-306">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-306">Windows 7</span></span><br/> <span data-ttu-id="feb39-307">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-307">Windows Vista</span></span><br/> <span data-ttu-id="feb39-308">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-308">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-309">Los juegos deben admitir escenarios estándar de multitarea de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-309">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-310">Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-310">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="feb39-311">Inicio > panel de control-> agregar o quitar cuentas de usuario-> crear una cuenta nueva</span><span class="sxs-lookup"><span data-stu-id="feb39-311">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="feb39-312">Inicie el juego como User Jane.</span><span class="sxs-lookup"><span data-stu-id="feb39-312">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="feb39-313">Presione ALT + TAB para volver al escritorio.</span><span class="sxs-lookup"><span data-stu-id="feb39-313">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="feb39-314">Compruebe que el juego está correctamente ALT + tabulaciones en el escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-314">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="feb39-315">Haga clic en Inicio-> [flecha a la derecha de bloquear]-> cambiar de usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-315">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="feb39-316">Inicie sesión como usuario Toby.</span><span class="sxs-lookup"><span data-stu-id="feb39-316">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="feb39-317">Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane.</span><span class="sxs-lookup"><span data-stu-id="feb39-317">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="feb39-318">Compruebe que el juego no encuentra errores para el usuario Toby o el usuario Julia durante el proceso de cambio de usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-318">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="feb39-319">Si puede iniciar otra sesión de juego, compruebe que no puede oír el audio de la sesión de juego original.</span><span class="sxs-lookup"><span data-stu-id="feb39-319">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="feb39-320">Cierre el juego y vuelva al usuario y el juego originales.</span><span class="sxs-lookup"><span data-stu-id="feb39-320">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="feb39-321">2,7 compatibilidad con nombres largos</span><span class="sxs-lookup"><span data-stu-id="feb39-321">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-322">Windows 7</span></span><br/> <span data-ttu-id="feb39-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-323">Windows Vista</span></span><br/> <span data-ttu-id="feb39-324">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-324">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-325">Si un juego admite el guardado de archivos, debe poder guardar archivos que tengan nombres y rutas de acceso largos.</span><span class="sxs-lookup"><span data-stu-id="feb39-325">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="feb39-326">El juego debe administrar correctamente caracteres especiales del sistema de archivos, como \/: \*?</span><span class="sxs-lookup"><span data-stu-id="feb39-326">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="feb39-327">&quot; < o > en los campos de entrada del usuario que se usan para crear nombres de archivo o rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="feb39-327">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-328">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-328">Launch the game.</span></span></li>
<li><span data-ttu-id="feb39-329">Inicie un nuevo juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-329">Start a new game.</span></span></li>
<li><span data-ttu-id="feb39-330">Guarde el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-330">Save the game.</span></span> <span data-ttu-id="feb39-331">Durante el proceso de almacenamiento, compruebe que el juego se guarda con el nombre guardar: mi primer juego guardar.</span><span class="sxs-lookup"><span data-stu-id="feb39-331">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="feb39-332">Vuelva al menú principal.</span><span class="sxs-lookup"><span data-stu-id="feb39-332">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="feb39-333">Intente cargar el juego recién guardado.</span><span class="sxs-lookup"><span data-stu-id="feb39-333">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="feb39-334">Compruebe que el juego no encuentra errores al controlar caracteres del sistema de archivos no admitidos, como \/: \*?</span><span class="sxs-lookup"><span data-stu-id="feb39-334">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="feb39-335">&quot; < o > si el juego lo permite, asigne un nombre al juego guardado.</span><span class="sxs-lookup"><span data-stu-id="feb39-335">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="feb39-336">Si el usuario puede asignar un nombre a su perfil o a caracteres o guardar juegos, compruebe que el juego no detecta errores al usar nombres de archivo largos aquí también.</span><span class="sxs-lookup"><span data-stu-id="feb39-336">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="feb39-337">3. instalación</span><span class="sxs-lookup"><span data-stu-id="feb39-337">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="feb39-338">Instalación sencilla de 3,1</span><span class="sxs-lookup"><span data-stu-id="feb39-338">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-339">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-339">Windows 7</span></span><br/> <span data-ttu-id="feb39-340">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-340">Windows Vista</span></span><br/> <span data-ttu-id="feb39-341">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-341">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-342">Los juegos con una instalación tradicional deben proporcionar una ruta de acceso simplificada en la interfaz de usuario del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-342">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-343">Inserte el disco del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-343">Insert the game disc.</span></span></li>
<li><span data-ttu-id="feb39-344">Compruebe que el juego no muestra más de un End-User contrato de licencia (CLUF).</span><span class="sxs-lookup"><span data-stu-id="feb39-344">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="feb39-345">Si el juego admite una opción de instalación personalizada o avanzada, compruebe que esta opción es accesible durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-345">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="feb39-346">Compruebe que la opción de instalación predeterminada omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, etc.).</span><span class="sxs-lookup"><span data-stu-id="feb39-346">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="feb39-347">Compruebe que el proceso de instalación del juego no solicita la instalación de los componentes del sistema operativo (instalación de DirectX, tiempos de ejecución de Visual C, etc.).</span><span class="sxs-lookup"><span data-stu-id="feb39-347">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="feb39-348">Compruebe que el proceso de instalación del juego no solicita interacción con el firewall.</span><span class="sxs-lookup"><span data-stu-id="feb39-348">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="feb39-349">Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-349">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="feb39-350">Compruebe que el proceso de desinstalación de juegos quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra todas las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="feb39-350">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="feb39-351">No es necesario limpiar todos los datos y la configuración de cada usuario (por ejemplo, los juegos guardados).</span><span class="sxs-lookup"><span data-stu-id="feb39-351">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="feb39-352">3,2 compatibilidad con el control de cuentas de usuario para la instalación</span><span class="sxs-lookup"><span data-stu-id="feb39-352">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-353">Windows 7</span></span><br/> <span data-ttu-id="feb39-354">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-354">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="feb39-355">El instalador del juego no debe asumir que se esté ejecutando en el mismo contexto que el usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-355">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="feb39-356">Por tanto, los juegos deben realizar tareas por usuario en la primera ejecución de forma independiente de la instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-356">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-357">Compruebe que puede instalar el juego como User Jane.</span><span class="sxs-lookup"><span data-stu-id="feb39-357">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="feb39-358">(Esto requerirá derechos elevados durante el proceso de instalación y configuración).</span><span class="sxs-lookup"><span data-stu-id="feb39-358">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="feb39-359">Compruebe que el proceso de instalación de juegos solicita al usuario Jane que eleve a través de las credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="feb39-359">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="feb39-360">(El mensaje de elevación se mostrará cuando el usuario intente instalar).</span><span class="sxs-lookup"><span data-stu-id="feb39-360">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="feb39-361">Optar por la ejecución automática del juego al final de la instalación, si aún no lo hace, o iniciarlo desde el menú que aparece.</span><span class="sxs-lookup"><span data-stu-id="feb39-361">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="feb39-362">Una vez en el juego, cree un nuevo perfil, juegue y guarde un juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-362">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="feb39-363">Salga del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-363">Exit the game.</span></span></li>
<li><span data-ttu-id="feb39-364">Reinicie el juego y compruebe que la cuenta de usuario Jane puede tener acceso a los perfiles de usuario y a los juegos guardados.</span><span class="sxs-lookup"><span data-stu-id="feb39-364">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="feb39-365">3,3 instalar en carpetas correctas</span><span class="sxs-lookup"><span data-stu-id="feb39-365">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-366">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-366">Windows 7</span></span><br/> <span data-ttu-id="feb39-367">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-367">Windows Vista</span></span><br/> <span data-ttu-id="feb39-368">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-368">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-369">De forma predeterminada, los juegos se deben instalar en la carpeta archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="feb39-369">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="feb39-370">Los datos de usuario se deben escribir en la primera ejecución y no durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-370">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-371">Instale el juego con el tipo de instalación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="feb39-371">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="feb39-372">Compruebe que el juego se ha instalado en los archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="feb39-372">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-373">Si se produce un error en esta prueba, compruebe que el juego esté diseñado para instalarse para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="feb39-373">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="feb39-374">Si es así, se trata de un error.</span><span class="sxs-lookup"><span data-stu-id="feb39-374">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="feb39-375">3,4 instalar los recursos de Windows correctamente</span><span class="sxs-lookup"><span data-stu-id="feb39-375">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-376">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-376">Windows 7</span></span><br/> <span data-ttu-id="feb39-377">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-377">Windows Vista</span></span><br/> <span data-ttu-id="feb39-378">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-378">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-379">Las aplicaciones no deben intentar instalar archivos o claves del registro protegidas por Protección de recursos de Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="feb39-379">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="feb39-380">Compruebe que no aparece ningún cuadro de diálogo de Protección de recursos de Windows WRP durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-380">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="feb39-381">3,5 evitar reinicios durante la instalación</span><span class="sxs-lookup"><span data-stu-id="feb39-381">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-382">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-382">Windows 7</span></span><br/> <span data-ttu-id="feb39-383">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-383">Windows Vista</span></span><br/> <span data-ttu-id="feb39-384">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-384">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-385">El instalador de juegos no debe suponer que la instalación de los componentes de Windows de los paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o la documentación de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="feb39-385">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-386">Instale el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-386">Install the game.</span></span></li>
<li><span data-ttu-id="feb39-387">Compruebe que el juego no requiere que el sistema se reinicie después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-387">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-388">Si una actualización de Microsoft System Update Redist requiere un reinicio, realice lo siguiente: complete la instalación del juego, desinstale el juego y vuelva a instalar el juego una segunda vez.</span><span class="sxs-lookup"><span data-stu-id="feb39-388">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="feb39-389">El proceso de instalación del juego no debe requerir un reinicio en esta segunda instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-389">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="feb39-390">3,6 usar el control de versiones de archivos correctamente</span><span class="sxs-lookup"><span data-stu-id="feb39-390">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-391">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-391">Windows 7</span></span><br/> <span data-ttu-id="feb39-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-392">Windows Vista</span></span><br/> <span data-ttu-id="feb39-393">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-393">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-394">El programa de instalación del juego debe comprobar correctamente para asegurarse de que las versiones más recientes del archivo estén instaladas.</span><span class="sxs-lookup"><span data-stu-id="feb39-394">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="feb39-395">La instalación de un juego nunca debe retrasar los archivos que no genere o que compartan las aplicaciones que no genere.</span><span class="sxs-lookup"><span data-stu-id="feb39-395">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-396">Antes de instalar el juego, cree una instantánea previa a la instalación de system32.</span><span class="sxs-lookup"><span data-stu-id="feb39-396">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-397">Cree un directorio denominado G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="feb39-397">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="feb39-398">Abra una ventana de comandos (Inicio > ejecutar > cmd).</span><span class="sxs-lookup"><span data-stu-id="feb39-398">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="feb39-399">Vaya a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="feb39-399">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="feb39-400">Escriba dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="feb39-400">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="feb39-401">Cree una instantánea posterior a la instalación de system32.</span><span class="sxs-lookup"><span data-stu-id="feb39-401">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="feb39-402">Abra una ventana de comandos (Inicio > ejecutar > cmd).</span><span class="sxs-lookup"><span data-stu-id="feb39-402">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="feb39-403">Vaya a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="feb39-403">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="feb39-404">Escriba dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="feb39-404">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="feb39-405">Compruebe que el juego no reproduce las versiones de archivo de los archivos que el juego no produjo (... de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="feb39-405">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="feb39-406">3,7 compatibilidad con el requisito condicional de ejecución automática \[\]</span><span class="sxs-lookup"><span data-stu-id="feb39-406">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-407">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-407">Windows 7</span></span><br/> <span data-ttu-id="feb39-408">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-408">Windows Vista</span></span><br/> <span data-ttu-id="feb39-409">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-409">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-410">En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admitan la ejecución automática, cuando se inserte el disco por primera vez, la aplicación debe ejecutarse automáticamente o solicitar al usuario que instale el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-410">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-411">Los programas de ejecución automática que se escribieron para usarse en versiones de Windows anteriores a Windows Vista no deben usar el tiempo de ejecución de .NET, ya que esta tecnología no se incluye con Windows XP o versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="feb39-411">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="feb39-412">Para obtener más información, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">juegos para Windows requisitos técnicos</a> 3,7, compatibilidad con la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="feb39-412">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="feb39-413">Inserte el disco de juego o el medio.</span><span class="sxs-lookup"><span data-stu-id="feb39-413">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="feb39-414">Compruebe que el cuadro de diálogo instalar/ejecutar aparece automáticamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-414">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="feb39-415">Windows Vista o Windows 7: Compruebe que el programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de las credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="feb39-415">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="feb39-416">Compruebe que el ejecutable de ejecución automática no necesita componentes de distribución no integrados, como .NET 3,5, C Run-Time bibliotecas, etc.</span><span class="sxs-lookup"><span data-stu-id="feb39-416">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="feb39-417">Compruebe que al volver a insertar el disco en la unidad después de la instalación no se inicia automáticamente la instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-417">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="feb39-418">4. confiabilidad</span><span class="sxs-lookup"><span data-stu-id="feb39-418">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="feb39-419">4,1 eliminación de los reinicios innecesarios</span><span class="sxs-lookup"><span data-stu-id="feb39-419">4.1 Eliminate Unnecessary Reboots</span></span>



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb39-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-420">Windows 7</span></span><br/> <span data-ttu-id="feb39-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-421">Windows Vista</span></span><br/> | <span data-ttu-id="feb39-422">Todos los instaladores de aplicaciones deben aprovechar las API del administrador de reinicio para evitar reinicios del sistema (consulte el [requisito 3,5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="feb39-422">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="feb39-423">4,2 eliminación de errores de comprobador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="feb39-423">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-424">Windows 7</span></span><br/> <span data-ttu-id="feb39-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-425">Windows Vista</span></span><br/> <span data-ttu-id="feb39-426">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-426">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-427">El juego no debe generar ningún error que se ejecute en Microsoft comprobador de aplicaciones (AppVerifier), versión 4,0 o posterior, en las siguientes pruebas:</span><span class="sxs-lookup"><span data-stu-id="feb39-427">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="feb39-428">Aspectos básicos: identificadores, montones, bloqueos, memoria, TLS</span><span class="sxs-lookup"><span data-stu-id="feb39-428">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="feb39-429">Varios: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="feb39-429">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-430">Herramienta de uso: AppVerifier 4,0 (o posterior)</span><span class="sxs-lookup"><span data-stu-id="feb39-430">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="feb39-431">Instale AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="feb39-431">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="feb39-432">Inicie AppVerifier y seleccione Archivo-> agregar aplicación.</span><span class="sxs-lookup"><span data-stu-id="feb39-432">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="feb39-433">Busque el archivo ejecutable del juego, selecciónelo y haga clic en el &quot; &quot; botón abrir.</span><span class="sxs-lookup"><span data-stu-id="feb39-433">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="feb39-434">En la &quot; &quot; sección aplicaciones, seleccione el archivo ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-434">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="feb39-435">En la &quot; sección de pruebas &quot; , seleccione las pruebas indicadas anteriormente en las categorías &quot; conceptos básicos &quot; y &quot; varios &quot; (desactive ThreadPool y TimeRollOver) y asegúrese de que las demás pruebas no estén seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="feb39-435">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="feb39-436">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-436">Launch the game.</span></span></li>
<li><span data-ttu-id="feb39-437">Compruebe que el juego no genera errores cuando se ejecuta en comprobador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="feb39-437">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="feb39-438">Algunas pruebas requieren que se ejecute completamente el depurador.</span><span class="sxs-lookup"><span data-stu-id="feb39-438">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="feb39-439">Esto puede requerir una versión de lanzamiento no protegida del archivo ejecutable del juego, ya que la tecnología antitrampa/antipiratería puede interferir con el AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="feb39-439">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="feb39-440">4,3 compatibilidad Informe de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="feb39-440">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-441">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-441">Windows 7</span></span><br/> <span data-ttu-id="feb39-442">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-442">Windows Vista</span></span><br/> <span data-ttu-id="feb39-443">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-443">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-444">Los juegos deben controlar solo las excepciones conocidas y esperadas, y Informe de errores de Windows no deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="feb39-444">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="feb39-445">Si se inserta un error (por ejemplo, una infracción de acceso) en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="feb39-445">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="feb39-446">Herramienta de uso: secuestrador de subprocesos</span><span class="sxs-lookup"><span data-stu-id="feb39-446">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="feb39-447">Si la aplicación se bloquea mientras se prueba, compruebe que el juego se muestre Informe de errores de Windows correctamente y recopile datos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="feb39-447">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-448">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-448">Windows 7</span></span><br/> <span data-ttu-id="feb39-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-449">Windows Vista</span></span><br/> <span data-ttu-id="feb39-450">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-450">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-451">Todos los archivos ejecutables (por ejemplo, archivos. exe o. dll) deben contener un nombre de producto exacto, el nombre de la compañía y la versión del archivo.</span><span class="sxs-lookup"><span data-stu-id="feb39-451">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="feb39-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Prueba manual:</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="feb39-453">Haga clic con el botón secundario en los archivos ejecutables del juego en el medio de instalación y en los instalados en el disco duro del equipo.</span><span class="sxs-lookup"><span data-stu-id="feb39-453">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="feb39-454">Seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb39-454">Select Properties.</span></span></li>
<li><span data-ttu-id="feb39-455">Windows XP: haga clic en la pestaña <strong>versión</strong> . Compruebe que los campos nombre de producto, nombre de la compañía y versión del archivo estén rellenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-455">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="feb39-456">Windows Vista o Windows 7: haga clic en la pestaña <strong>detalles</strong> . Compruebe que los campos nombre del producto y versión del archivo estén rellenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-456">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="feb39-457">El nombre de la compañía no es visible en la página de propiedades de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb39-457">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="feb39-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Prueba automatizada:</dt> </span><span class="sxs-lookup"><span data-stu-id="feb39-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="feb39-459">Usar la herramienta Microsoft Games for Windows Test; Vea la <a href="#64-microsoft-games-for-windows-test-tool">sección 6,4</a>.</span><span class="sxs-lookup"><span data-stu-id="feb39-459">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feb39-460">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-460">Windows 7</span></span><br/> <span data-ttu-id="feb39-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb39-461">Windows Vista</span></span><br/> <span data-ttu-id="feb39-462">Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-462">Windows XP</span></span><br/></td>
<td><span data-ttu-id="feb39-463">La salida normal del juego no debe producir un error de excepción desconocido.</span><span class="sxs-lookup"><span data-stu-id="feb39-463">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="feb39-464">Después de reproducir el juego para una sesión de juego normal, compruebe que el juego no genera errores al salir.</span><span class="sxs-lookup"><span data-stu-id="feb39-464">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="feb39-465">5. script de prueba de ejemplo</span><span class="sxs-lookup"><span data-stu-id="feb39-465">5. Sample Test Script</span></span>

<span data-ttu-id="feb39-466">Este es un ejemplo de un paso de prueba típico que usa los requisitos de prueba anteriores como guía.</span><span class="sxs-lookup"><span data-stu-id="feb39-466">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="feb39-467">5,1 herramientas</span><span class="sxs-lookup"><span data-stu-id="feb39-467">5.1 Tools</span></span>

-   <span data-ttu-id="feb39-468">edición de 32 bits de Windows Vista SP1 y/o Windows 7 en una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="feb39-468">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="feb39-469">edición de 32 bits de Windows Vista SP1 y/o Windows 7 en una CPU de Intel</span><span class="sxs-lookup"><span data-stu-id="feb39-469">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="feb39-470">edición de 64 bits de Windows Vista SP1 y/o Windows 7 en una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="feb39-470">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="feb39-471">edición de 64 bits de Windows Vista SP1 y/o Windows 7 en una CPU de Intel</span><span class="sxs-lookup"><span data-stu-id="feb39-471">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="feb39-472">edición de 32 bits de Windows XP SP2 en una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="feb39-472">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="feb39-473">edición de 32 bits de Windows XP SP2 en una CPU de Intel</span><span class="sxs-lookup"><span data-stu-id="feb39-473">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="feb39-474">Monitor de pantalla ancha compatible con 1680 1050</span><span class="sxs-lookup"><span data-stu-id="feb39-474">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="feb39-475">Controladora Xbox 360 para Windows</span><span class="sxs-lookup"><span data-stu-id="feb39-475">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="feb39-476">5,2 preinstalación</span><span class="sxs-lookup"><span data-stu-id="feb39-476">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="feb39-477">Windows Vista y Windows 7: crear dos usuarios estándar: Julia y Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-477">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="feb39-478">Windows Vista y Windows 7: comprobación de que el control de cuentas de usuario está habilitado</span><span class="sxs-lookup"><span data-stu-id="feb39-478">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="feb39-479">Crear una instantánea previa a la instalación de system32</span><span class="sxs-lookup"><span data-stu-id="feb39-479">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="feb39-480">Cree un directorio denominado G4Wtest</span><span class="sxs-lookup"><span data-stu-id="feb39-480">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="feb39-481">Abrir una ventana de comandos (Inicio > ejecutar > cmd)</span><span class="sxs-lookup"><span data-stu-id="feb39-481">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="feb39-482">Vaya a c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="feb39-482">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="feb39-483">Escriba dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="feb39-483">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="feb39-484">Windows Vista y Windows 7: establezca en 150% DPI \[ 1,8\]</span><span class="sxs-lookup"><span data-stu-id="feb39-484">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="feb39-485">Continuar con la [instalación](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="feb39-485">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="feb39-486">instalación de 5,3</span><span class="sxs-lookup"><span data-stu-id="feb39-486">5.3 Install</span></span>

1.  <span data-ttu-id="feb39-487">Iniciar sesión como usuario Julia</span><span class="sxs-lookup"><span data-stu-id="feb39-487">Log on as User Jane</span></span>
2.  <span data-ttu-id="feb39-488">Inserte el disco del juego en la unidad de CD/DVD, compruebe que el cuadro de diálogo instalar/ejecutar aparece automáticamente \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="feb39-488">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="feb39-489">Compruebe que el proceso de instalación de juego solicita al usuario Julia que eleve las credenciales de administrador \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-489">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="feb39-490">Compruebe que el programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de las credenciales de administrador \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="feb39-490">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="feb39-491">Compruebe que el juego no muestra más de un End-User contrato de licencia (EULA) \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-491">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="feb39-492">Compruebe que el juego muestra opciones de instalación predeterminadas, sencillas y personalizadas y avanzadas \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-492">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="feb39-493">Compruebe que la opción de instalación predeterminada o fácil omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, etc.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-493">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="feb39-494">Compruebe que el proceso de instalación del juego no solicita la instalación de los componentes del sistema operativo (instalación de DirectX, bibliotecas de C Run-Time, etc.) \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-494">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="feb39-495">Compruebe que el proceso de instalación del juego no solicita la interacción con el Firewall \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-495">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="feb39-496">Compruebe que el proceso de instalación del juego no encuentra un error relacionado con la versión del sistema operativo \[ 2,5 \] \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-496">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="feb39-497">Compruebe que el proceso de instalación del juego no muestra cuadros de diálogo de controladores sin firmar \[ 2,4\]</span><span class="sxs-lookup"><span data-stu-id="feb39-497">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="feb39-498">Compruebe que no aparece ningún cuadro de diálogo de Protección de recursos de Windows (WRP) durante el proceso de instalación \[ 3,4\]</span><span class="sxs-lookup"><span data-stu-id="feb39-498">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="feb39-499">Compruebe que la reinserción del disco en la unidad después de la instalación no hace que la instalación se inicie automáticamente de nuevo.</span><span class="sxs-lookup"><span data-stu-id="feb39-499">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="feb39-500">Comprobar que el juego no requiere que el sistema se reinicie después de la instalación \[ 3,5\]</span><span class="sxs-lookup"><span data-stu-id="feb39-500">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="feb39-501">Compruebe que puede instalar el juego como usuario Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-501">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="feb39-502">Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-502">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="feb39-503">Si el juego se ejecuta automáticamente después de la instalación, vaya al [tiempo de ejecución](#55-runtime) .</span><span class="sxs-lookup"><span data-stu-id="feb39-503">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="feb39-504">Si el juego dejó un menú de inicio o no se pudo desinstalar, consulte la sección [posterior a la instalación](#54-post-install) .</span><span class="sxs-lookup"><span data-stu-id="feb39-504">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="feb39-505">5,4 posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="feb39-505">5.4 Post-Install</span></span>

1.  <span data-ttu-id="feb39-506">Compruebe que el juego no coloca accesos directos de inicio en el escritorio de usuario \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-506">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="feb39-507">Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-507">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="feb39-508">Comprobar que el icono de juego aparece en el explorador de juegos de Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-508">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="feb39-509">Compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) de la parte inferior se muestran y son correctos \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-509">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="feb39-510">Compruebe que el icono de juego muestra información de Windows Experience index (WEI) en el explorador de juegos de Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-510">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="feb39-511">Comprobar que los hipervínculos de juego para metadatos funcionan correctamente en el explorador de juegos de Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-511">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="feb39-512">Compruebe que el juego muestra la clasificación de control parental exacta en el explorador de juegos de Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-512">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="feb39-513">Crear una instantánea posterior a la instalación de system32</span><span class="sxs-lookup"><span data-stu-id="feb39-513">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="feb39-514">Abrir una ventana de comandos (Inicio > ejecutar > cmd)</span><span class="sxs-lookup"><span data-stu-id="feb39-514">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="feb39-515">Vaya a c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="feb39-515">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="feb39-516">Escriba dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="feb39-516">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="feb39-517">Compruebe que el juego no retrase las versiones de archivo de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt \[ 3,6\]</span><span class="sxs-lookup"><span data-stu-id="feb39-517">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="feb39-518">Continuar en [tiempo de ejecución](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="feb39-518">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="feb39-519">tiempo de ejecución de 5,5</span><span class="sxs-lookup"><span data-stu-id="feb39-519">5.5 Runtime</span></span>

1.  <span data-ttu-id="feb39-520">Tiempo de ejecución 1: Si el menú Inicio está presente, inicie el juego desde allí.</span><span class="sxs-lookup"><span data-stu-id="feb39-520">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="feb39-521">Si el juego se ejecutó automáticamente o se inició desde el menú del selector de juegos después de la instalación, realice lo siguiente: Si no es así, vaya al tiempo de ejecución 2:</span><span class="sxs-lookup"><span data-stu-id="feb39-521">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="feb39-522">Crear un perfil (si el juego lo permite)</span><span class="sxs-lookup"><span data-stu-id="feb39-522">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="feb39-523">Iniciar un nuevo juego</span><span class="sxs-lookup"><span data-stu-id="feb39-523">Start a new game</span></span>
    3.  <span data-ttu-id="feb39-524">Guardar el juego</span><span class="sxs-lookup"><span data-stu-id="feb39-524">Save the game</span></span>
    4.  <span data-ttu-id="feb39-525">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-525">Exit the game</span></span>
    5.  <span data-ttu-id="feb39-526">Iniciar el juego desde el explorador de juegos</span><span class="sxs-lookup"><span data-stu-id="feb39-526">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="feb39-527">Compruebe que el juego se inicia desde el icono del explorador de juegos \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-527">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="feb39-528">Compruebe que el juego no solicita credenciales de administrador en el inicio \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-528">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="feb39-529">Compruebe que se puede tener acceso a los perfiles de usuario y guardar los juegos mediante la cuenta de usuario Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-529">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="feb39-530">Continuar en tiempo de ejecución 3</span><span class="sxs-lookup"><span data-stu-id="feb39-530">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="feb39-531">Tiempo de ejecución 2: Si el juego no se ejecutó automáticamente o muestra un inicio en el menú del selector de juegos, se trata de un error de \[ 3,1 \] ; sin embargo, las pruebas pueden continuar normalmente:</span><span class="sxs-lookup"><span data-stu-id="feb39-531">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="feb39-532">Iniciar el juego desde el explorador de juegos</span><span class="sxs-lookup"><span data-stu-id="feb39-532">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="feb39-533">Compruebe que el juego se inicia desde el icono del explorador de juegos \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-533">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="feb39-534">Compruebe que el juego no solicita credenciales de administrador en el inicio \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-534">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="feb39-535">Continuar en tiempo de ejecución 3</span><span class="sxs-lookup"><span data-stu-id="feb39-535">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="feb39-536">Tiempo de ejecución 3: Si el juego es compatible con un panel de juego, compruebe que el juego reconoce la controladora Xbox 360 para Windows como dispositivo de entrada \[ 1,4\]</span><span class="sxs-lookup"><span data-stu-id="feb39-536">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="feb39-537">Si es necesario, habilite el controlador a través del menú opciones.</span><span class="sxs-lookup"><span data-stu-id="feb39-537">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="feb39-538">Comprobar que el juego hace referencia a los botones del controlador y a los desencadenadores mediante los nombres de Xbox 360</span><span class="sxs-lookup"><span data-stu-id="feb39-538">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="feb39-539">Comprobar que el juego y el sistema de menús se pueden controlar con la controladora Xbox 360 para Windows</span><span class="sxs-lookup"><span data-stu-id="feb39-539">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="feb39-540">Compruebe que la controladora Xbox 360 para Windows se comporta de acuerdo con los estándares aceptados.</span><span class="sxs-lookup"><span data-stu-id="feb39-540">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="feb39-541">Establezca el vídeo en \[ 1,5 \] :</span><span class="sxs-lookup"><span data-stu-id="feb39-541">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="feb39-542">Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3 (800 600 o 1024 768).</span><span class="sxs-lookup"><span data-stu-id="feb39-542">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="feb39-543">Compruebe que el juego se ejecuta con una resolución de relación de aspecto 16:9 (1280 720).</span><span class="sxs-lookup"><span data-stu-id="feb39-543">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="feb39-544">Compruebe que el juego se ejecuta con una resolución de relación de aspecto 16:10 (1680 1050, 800 480 o 1152 720)</span><span class="sxs-lookup"><span data-stu-id="feb39-544">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="feb39-545">Comprobar que el juego solicita al usuario cuando se realiza un cambio en la resolución</span><span class="sxs-lookup"><span data-stu-id="feb39-545">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="feb39-546">Compruebe que la pantalla revierte a la configuración anterior si no acepta en 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="feb39-546">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="feb39-547">Compruebe que el juego no estire la imagen y, a su vez, presente un área más amplia de la vista</span><span class="sxs-lookup"><span data-stu-id="feb39-547">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="feb39-548">Comprobar que el juego no agrega barras negras a la izquierda y a la derecha del área de juego</span><span class="sxs-lookup"><span data-stu-id="feb39-548">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="feb39-549">Si está disponible en la configuración de vídeo, compruebe que las opciones de representación de juego tienen como valor predeterminado Direct3D \[ 1,7 \] ; de lo contrario, continúe con las [pruebas automatizadas](#58-automated-tests) .</span><span class="sxs-lookup"><span data-stu-id="feb39-549">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="feb39-550">Si se le solicita o si la opción está disponible, cree un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="feb39-550">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="feb39-551">Compruebe que el juego no encuentra errores al usar nombres de archivo largos \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="feb39-551">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="feb39-552">Inicie un nuevo juego, cree un juego y compruebe que el juego no encuentre errores al controlar los caracteres del sistema de archivos no admitidos \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="feb39-552">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="feb39-553">Compruebe que el juego está correctamente ALT + pestañas en el escritorio de Windows \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="feb39-553">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="feb39-554">Cambiar a los usuarios con el juego en ejecución haciendo clic en Inicio-> cambiar usuario</span><span class="sxs-lookup"><span data-stu-id="feb39-554">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="feb39-555">Iniciar sesión como Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-555">Log on as Toby</span></span>
    3.  <span data-ttu-id="feb39-556">Comprobar que el juego se inicia como usuario Toby mientras se sigue ejecutando como usuario Jane \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="feb39-556">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="feb39-557">Compruebe que el juego no encuentra errores para el usuario Toby o el usuario Julia durante el proceso de cambio de usuario \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="feb39-557">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="feb39-558">Compruebe que no puede oír el audio de la sesión de juego original \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="feb39-558">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="feb39-559">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-559">Exit the game</span></span>
    7.  <span data-ttu-id="feb39-560">Cerrar sesión Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-560">Log off Toby</span></span>
    8.  <span data-ttu-id="feb39-561">Vuelva al usuario original en el que se está ejecutando el juego</span><span class="sxs-lookup"><span data-stu-id="feb39-561">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="feb39-562">Presione ALT + TAB para volver al juego</span><span class="sxs-lookup"><span data-stu-id="feb39-562">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="feb39-563">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-563">Exit the game</span></span>
10. <span data-ttu-id="feb39-564">Continuar en [el tiempo de ejecución](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="feb39-564">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="feb39-565">5,6 posterior al tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="feb39-565">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="feb39-566">Compruebe que el juego no genera errores al salir \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-566">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="feb39-567">Comprobar que el juego está instalado en los archivos de programa \[ 3,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-567">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="feb39-568">Continuar con el [control parental](/windows)</span><span class="sxs-lookup"><span data-stu-id="feb39-568">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="feb39-569">Controles parentales de 5,7</span><span class="sxs-lookup"><span data-stu-id="feb39-569">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="feb39-570">Abrir controles parentales en el panel de control</span><span class="sxs-lookup"><span data-stu-id="feb39-570">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="feb39-571">Compruebe que el juego muestra la clasificación de control parental exacta debajo del título del juego en el panel de control de controles parentales \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-571">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="feb39-572">Vea el caso \[ de prueba 1,2 \] para las siguientes pruebas:</span><span class="sxs-lookup"><span data-stu-id="feb39-572">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="feb39-573">Después de establecer el control parental en "ON", compruebe que el juego se ejecuta con esta configuración como usuario Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-573">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="feb39-574">Cerrar sesión e iniciar sesión como Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-574">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="feb39-575">Compruebe que el juego se ejecuta con esta configuración como usuario Toby \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-575">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="feb39-576">Cerrar sesión e iniciar sesión como Julia</span><span class="sxs-lookup"><span data-stu-id="feb39-576">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="feb39-577">En la sección Control parental, bloquee la Toby del usuario para ver los juegos de un ESRB de nivel superior y superior del juego que acaba de instalar.</span><span class="sxs-lookup"><span data-stu-id="feb39-577">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="feb39-578">Ejemplo: Si el juego tiene la clasificación E, establézcalo de modo que Toby solo pueda jugar a juegos con la clasificación C</span><span class="sxs-lookup"><span data-stu-id="feb39-578">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="feb39-579">Compruebe que el juego se ejecuta con esta configuración como usuario Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-579">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="feb39-580">Cerrar sesión e iniciar sesión como usuario Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-580">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="feb39-581">Compruebe que el juego no se inicia en el usuario Toby cuando ESRB está bloqueado por el usuario Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-581">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="feb39-582">Cerrar sesión como usuario Toby y volver a iniciar como usuario Julia</span><span class="sxs-lookup"><span data-stu-id="feb39-582">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="feb39-583">Si ha cambiado previamente, restaure la configuración de ESRB</span><span class="sxs-lookup"><span data-stu-id="feb39-583">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="feb39-584">Si no hay ninguna configuración de ESRB, seleccione "bloquear o permitir juegos específicos" y seleccione el juego por nombre.</span><span class="sxs-lookup"><span data-stu-id="feb39-584">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="feb39-585">Cierre la sesión como Jane y on como Toby</span><span class="sxs-lookup"><span data-stu-id="feb39-585">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="feb39-586">Compruebe que el juego no se inicia en el usuario Toby cuando el usuario Jane 1,2 bloquea el archivo EXE/Name. \[\]</span><span class="sxs-lookup"><span data-stu-id="feb39-586">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="feb39-587">Cierre la sesión como Toby y vuelva a iniciarla como Julia</span><span class="sxs-lookup"><span data-stu-id="feb39-587">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="feb39-588">Como Julia, abra controles de usuario-> restricciones de la aplicación</span><span class="sxs-lookup"><span data-stu-id="feb39-588">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="feb39-589">Haga clic en "Toby solo puede usar los programas que se permiten" y, a continuación, haga clic en Aceptar (es decir, no permitir ningún exe)</span><span class="sxs-lookup"><span data-stu-id="feb39-589">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="feb39-590">Haga clic en el cuadro desactive todo y, a continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="feb39-590">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="feb39-591">Vaya a controles de usuario \| juegos controles y permita el juego específico con la Clasificación ESRB</span><span class="sxs-lookup"><span data-stu-id="feb39-591">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="feb39-592">Cierre la sesión como Julia e inicie sesión como Toby e intente jugar al juego</span><span class="sxs-lookup"><span data-stu-id="feb39-592">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="feb39-593">Compruebe que el juego no esté bloqueado y que Toby pueda reproducirlo cuando "no permitir ningún exe" esté establecido en \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-593">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="feb39-594">Cerrar sesión como usuario Toby y volver a iniciar como usuario Julia</span><span class="sxs-lookup"><span data-stu-id="feb39-594">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="feb39-595">Vaya a controles parentales en el panel de control y quite las restricciones</span><span class="sxs-lookup"><span data-stu-id="feb39-595">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="feb39-596">Comprobar que los dos usuarios ya pueden jugar al juego</span><span class="sxs-lookup"><span data-stu-id="feb39-596">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="feb39-597">Continuar con las [pruebas automatizadas](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="feb39-597">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="feb39-598">5,8 pruebas automatizadas</span><span class="sxs-lookup"><span data-stu-id="feb39-598">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="feb39-599">Compruebe que el juego no genera errores cuando se ejecuta en comprobador de aplicaciones; vea la documentación de la herramienta de pruebas de personalización de marca \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="feb39-599">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="feb39-600">Compruebe que los archivos ejecutables del juego contienen manifiestos; vea la documentación de la herramienta de pruebas de personalización de marca \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-600">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="feb39-601">Compruebe que el archivo ejecutable del juego requestedExecutionLevel es "AsInvoker"; vea la documentación de la herramienta de prueba de marca \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-601">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="feb39-602">Continuar con [otras pruebas](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="feb39-602">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="feb39-603">5,9 otras pruebas</span><span class="sxs-lookup"><span data-stu-id="feb39-603">5.9 Other Tests</span></span>

1.  <span data-ttu-id="feb39-604">Compruebe que los archivos ejecutables del juego contienen una firma digital \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-604">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="feb39-605">Comprobar que el proceso de instalación de juego se ejecuta normalmente en las ediciones de 64 bits de Windows Vista y/o Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-605">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="feb39-606">Compruebe que el juego no encuentra un error como resultado de los ejecutables de 16 bits en las ediciones de 64 bits de Windows Vista y/o Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-606">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="feb39-607">Forzar la aplicación para que se bloquee durante las pruebas y comprobar que el juego se muestra Informe de errores de Windows correctamente y recopila los datos de bloqueo \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-607">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="feb39-608">Asegúrese de que los resúmenes de archivo sean correctos \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-608">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="feb39-609">Haga clic en Inicio-> equipo</span><span class="sxs-lookup"><span data-stu-id="feb39-609">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="feb39-610">Navegue hasta el directorio del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-610">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="feb39-611">En la ventana Buscar, escriba \* . dll</span><span class="sxs-lookup"><span data-stu-id="feb39-611">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="feb39-612">Para cada archivo: haga clic con el botón derecho en el archivo y haga clic en propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb39-612">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="feb39-613">En Windows XP: haga clic en la pestaña versión. Compruebe que los campos nombre de producto, nombre de la compañía y versión del archivo estén rellenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-613">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="feb39-614">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-614">\[4.3\]</span></span>
        -   <span data-ttu-id="feb39-615">En Windows Vista y Windows 7: haga clic en la pestaña detalles. Compruebe que los campos nombre del producto y versión del archivo estén rellenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="feb39-615">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="feb39-616">El nombre de la compañía no es visible en la página de propiedades de Windows Vista o Windows 7 \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="feb39-616">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="feb39-617">Repetir esta comprobación para los archivos. exe</span><span class="sxs-lookup"><span data-stu-id="feb39-617">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="feb39-618">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-618">Launch the game.</span></span>

    1.  <span data-ttu-id="feb39-619">Presione CTRL + ALT + SUPR</span><span class="sxs-lookup"><span data-stu-id="feb39-619">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="feb39-620">Haga clic en la flecha "opciones de apagado"</span><span class="sxs-lookup"><span data-stu-id="feb39-620">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="feb39-621">Haga clic en reiniciar</span><span class="sxs-lookup"><span data-stu-id="feb39-621">Click Restart</span></span>
    4.  <span data-ttu-id="feb39-622">Compruebe que el juego no bloquee el cierre \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-622">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="feb39-623">Continuar con la [desinstalación](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="feb39-623">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="feb39-624">5,10 desinstalación</span><span class="sxs-lookup"><span data-stu-id="feb39-624">5.10 Uninstall</span></span>

-   <span data-ttu-id="feb39-625">Compruebe que el proceso de desinstalación de juegos quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra todas las opciones de configuración \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-625">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="feb39-626">Comprobar en Windows Vista o Windows 7 que el panel de control es la única manera de quitar el programa \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="feb39-626">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="feb39-627">Notas de la herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="feb39-627">Test Tool Notes</span></span>

<span data-ttu-id="feb39-628">Estas son las notas para cada una de las herramientas de prueba que se enumeran en los requisitos de pruebas anteriores.</span><span class="sxs-lookup"><span data-stu-id="feb39-628">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="feb39-629">6,1 AppVerifier 4,0 (o superior)</span><span class="sxs-lookup"><span data-stu-id="feb39-629">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="feb39-630">**Caso de prueba: 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="feb39-630">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="feb39-631">Algunas aplicaciones no se ejecutan con AppVerifier ejecutándose debido a la protección contra copia.</span><span class="sxs-lookup"><span data-stu-id="feb39-631">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="feb39-632">Esto se puede resolver ejecutando con una versión de lanzamiento sin protección del ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-632">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="feb39-633">Instalación de AppVerifier 4,0 (o posterior) en un equipo que ejecuta Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb39-633">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="feb39-634">Inicie AppVerifier y haga clic en archivo-> agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="feb39-634">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="feb39-635">Busque el archivo ejecutable del juego, selecciónelo y haga clic en abrir.</span><span class="sxs-lookup"><span data-stu-id="feb39-635">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="feb39-636">En la sección "aplicaciones", seleccione el archivo ejecutable del juego</span><span class="sxs-lookup"><span data-stu-id="feb39-636">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="feb39-637">Seleccione las siguientes pruebas en la sección "aspectos básicos":</span><span class="sxs-lookup"><span data-stu-id="feb39-637">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="feb39-638">Asas</span><span class="sxs-lookup"><span data-stu-id="feb39-638">Handles</span></span>
    -   <span data-ttu-id="feb39-639">Montones</span><span class="sxs-lookup"><span data-stu-id="feb39-639">Heaps</span></span>
    -   <span data-ttu-id="feb39-640">Bloqueos</span><span class="sxs-lookup"><span data-stu-id="feb39-640">Locks</span></span>
    -   <span data-ttu-id="feb39-641">Memory</span><span class="sxs-lookup"><span data-stu-id="feb39-641">Memory</span></span>
    -   <span data-ttu-id="feb39-642">TLS</span><span class="sxs-lookup"><span data-stu-id="feb39-642">TLS</span></span>

6.  <span data-ttu-id="feb39-643">Seleccione las siguientes pruebas en la sección "varios":</span><span class="sxs-lookup"><span data-stu-id="feb39-643">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="feb39-644">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="feb39-644">DangerousAPIs</span></span>
    -   <span data-ttu-id="feb39-645">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="feb39-645">DirtyStacks</span></span>

7.  <span data-ttu-id="feb39-646">Asegúrese de que todas las demás pruebas no estén seleccionadas</span><span class="sxs-lookup"><span data-stu-id="feb39-646">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="feb39-647">Iniciar el juego</span><span class="sxs-lookup"><span data-stu-id="feb39-647">Launch the game</span></span>
9.  <span data-ttu-id="feb39-648">Juego</span><span class="sxs-lookup"><span data-stu-id="feb39-648">Play the game</span></span>
10. <span data-ttu-id="feb39-649">Cierre el juego</span><span class="sxs-lookup"><span data-stu-id="feb39-649">Close the game</span></span>
11. <span data-ttu-id="feb39-650">En AppVerifier, seleccione Ver registros de ></span><span class="sxs-lookup"><span data-stu-id="feb39-650">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="feb39-651">En la sección "aplicaciones", seleccione el archivo app. exe.</span><span class="sxs-lookup"><span data-stu-id="feb39-651">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="feb39-652">En la sección "registros", seleccione el archivo de registro y observe el recuento de errores.</span><span class="sxs-lookup"><span data-stu-id="feb39-652">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="feb39-653">Si no hay ningún error, finalice las pruebas de AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="feb39-653">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="feb39-654">Si hay errores, haga clic en el botón ver</span><span class="sxs-lookup"><span data-stu-id="feb39-654">If there are errors, click the View button</span></span>
14. <span data-ttu-id="feb39-655">Buscar el documento (CTRL + F) para Severity = "error</span><span class="sxs-lookup"><span data-stu-id="feb39-655">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="feb39-656">Crear errores basados en la parte LayerName = del error</span><span class="sxs-lookup"><span data-stu-id="feb39-656">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="feb39-657">Prueba del manifiesto 6,2: mt.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-657">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="feb39-658">**Caso de prueba: 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="feb39-658">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="feb39-659">Esta herramienta se ejecuta desde un símbolo del sistema donde se encuentra MT.exe.</span><span class="sxs-lookup"><span data-stu-id="feb39-659">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="feb39-660">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="feb39-660">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="feb39-661">Haga clic en Inicio > ejecutar > escriba cmd y haga clic en el botón Aceptar.</span><span class="sxs-lookup"><span data-stu-id="feb39-661">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="feb39-662">Ejecute la herramienta de mt.exe para generar un archivo. manifest para cada archivo. exe que se instala con el juego</span><span class="sxs-lookup"><span data-stu-id="feb39-662">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="feb39-663">Abra el archivo. manifest generado.</span><span class="sxs-lookup"><span data-stu-id="feb39-663">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="feb39-664">Asegúrese de que cada archivo. exe contiene lo siguiente (solicitado:</span><span class="sxs-lookup"><span data-stu-id="feb39-664">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="feb39-665">El nivel de ejecución solicitado debe estar presente para cada archivo y dpiAware debe estar presente al menos en el archivo ejecutable del juego s.</span><span class="sxs-lookup"><span data-stu-id="feb39-665">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="feb39-666">6,3 secuestrador de subprocesos: threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-666">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="feb39-667">Esta herramienta se ejecuta desde un símbolo del sistema donde se encuentra threadhijacker.exe.</span><span class="sxs-lookup"><span data-stu-id="feb39-667">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="feb39-668">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="feb39-668">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="feb39-669">Donde str es el nombre \_ de \_program.exe</span><span class="sxs-lookup"><span data-stu-id="feb39-669">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="feb39-670">Abra el administrador de tareas, haga clic en la pestaña procesos y busque el nombre del ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="feb39-670">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="feb39-671">Abra un símbolo del sistema en modo de administrador.</span><span class="sxs-lookup"><span data-stu-id="feb39-671">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="feb39-672">Navegue al directorio donde threadhijacker.exe es</span><span class="sxs-lookup"><span data-stu-id="feb39-672">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="feb39-673">Escriba: **threadhijacker.exe/Process:** Str, donde str es el nombre del ejecutable que desea alcanzar.</span><span class="sxs-lookup"><span data-stu-id="feb39-673">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="feb39-674">6,4 Microsoft Games for Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="feb39-674">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="feb39-675">Esta herramienta se encuentra en el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="feb39-675">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="feb39-676">Una vez que el SDK está instalado en un equipo, el instalador de la herramienta de prueba games for Windows se puede colocar en el equipo de pruebas e instalar.</span><span class="sxs-lookup"><span data-stu-id="feb39-676">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="feb39-677">Busque el instalador de Microsoft Games for Windows Test Tool en el equipo de desarrollo en el que está instalado el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="feb39-677">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="feb39-678">De forma predeterminada, se coloca en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="feb39-678">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="feb39-679">Copie el instalador (MicrosoftGFWTestTool.msi/setup.exe) en el equipo de pruebas.</span><span class="sxs-lookup"><span data-stu-id="feb39-679">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="feb39-680">Ejecute al programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="feb39-680">Run the installer.</span></span>
3.  <span data-ttu-id="feb39-681">Inicie la herramienta Microsoft Games for Windows Test.</span><span class="sxs-lookup"><span data-stu-id="feb39-681">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="feb39-682">En el campo **lista de proyectos** , reemplace **crear nuevo proyecto** por el nombre del título y haga clic en **crear nuevo**.</span><span class="sxs-lookup"><span data-stu-id="feb39-682">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="feb39-683">Espere a que se complete la línea base.</span><span class="sxs-lookup"><span data-stu-id="feb39-683">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="feb39-684">Rellene la información que pueda tener en la sección **información del juego** y haga clic en **Actualizar información de juego**.</span><span class="sxs-lookup"><span data-stu-id="feb39-684">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="feb39-685">Haga clic en la pestaña **casos de prueba** .</span><span class="sxs-lookup"><span data-stu-id="feb39-685">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="feb39-686">A partir de la parte superior, continúe a través de los casos de prueba y haga clic en **correcto** o en **error** según corresponda.</span><span class="sxs-lookup"><span data-stu-id="feb39-686">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="feb39-687">Vea "escribir un error" más adelante en esta sección para obtener más información sobre cómo incluir un error en el informe.</span><span class="sxs-lookup"><span data-stu-id="feb39-687">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="feb39-688">Vuelva a la pestaña **proyectos** después de revisar el informe (activando las pestañas de **edición** de **informes** y errores).</span><span class="sxs-lookup"><span data-stu-id="feb39-688">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="feb39-689">Haga clic en **compilar Informe**.</span><span class="sxs-lookup"><span data-stu-id="feb39-689">Click **Compile Report**.</span></span>

    <span data-ttu-id="feb39-690">Se abrirá una ventana cuando el informe termine de compilarse.</span><span class="sxs-lookup"><span data-stu-id="feb39-690">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="feb39-691">Aquí encontrará un. Nombres de archivo ZIP *ProjectName* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="feb39-691">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="feb39-692">Este archivo contiene todos los registros y resultados recopilados durante la prueba superada.</span><span class="sxs-lookup"><span data-stu-id="feb39-692">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="feb39-693">Escribir un error</span><span class="sxs-lookup"><span data-stu-id="feb39-693">Writing a Bug</span></span>

<span data-ttu-id="feb39-694">Hay dos maneras de escribir un informe de errores: puede pasar por los casos de prueba y hacer clic en **error** si el título no es un caso de prueba, o puede hacer clic en la pestaña **Editar error** y agregar manualmente un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="feb39-694">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="feb39-695">Hacer clic en error en un caso de prueba</span><span class="sxs-lookup"><span data-stu-id="feb39-695">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="feb39-696">Al hacer clic en **error** en un caso de prueba, la lista desplegable **tipo de problema** se establecerá automáticamente en el tipo de caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="feb39-696">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="feb39-697">Agregue una descripción breve al campo de **título** que describa brevemente el problema.</span><span class="sxs-lookup"><span data-stu-id="feb39-697">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="feb39-698">Agregue una descripción detallada del problema al campo **comportamiento observado** .</span><span class="sxs-lookup"><span data-stu-id="feb39-698">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="feb39-699">Según corresponda, agregue lo que se esperaba (en lugar de una descripción del problema) al campo **comportamiento esperado** .</span><span class="sxs-lookup"><span data-stu-id="feb39-699">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="feb39-700">Agregue una descripción detallada de cómo reproducir el problema en el campo **reproducción-pasos** .</span><span class="sxs-lookup"><span data-stu-id="feb39-700">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="feb39-701">Cuando haya terminado, haga clic en el botón **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="feb39-701">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="feb39-702">Agregar manualmente un error</span><span class="sxs-lookup"><span data-stu-id="feb39-702">Manually Adding a Bug</span></span>

<span data-ttu-id="feb39-703">Este proceso es el mismo que cuando se hace clic en **FAIL**, con la excepción de la lista desplegable de rellenado automático.</span><span class="sxs-lookup"><span data-stu-id="feb39-703">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="feb39-704">En este caso, seleccione el tipo de error de TCR adecuado o seleccione un **\* \* problema \* \* que no sea TR** para los errores que se encuentren fuera del intervalo TR, pero que todavía se deben informar.</span><span class="sxs-lookup"><span data-stu-id="feb39-704">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="feb39-705">Recursos</span><span class="sxs-lookup"><span data-stu-id="feb39-705">Resources</span></span>

<dl> <dt>

<span data-ttu-id="feb39-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Juegos para Windows: requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="feb39-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="feb39-707">Juegos para requisitos técnicos de Windows: prácticas recomendadas para juegos en Windows XP, Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="feb39-707">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="feb39-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="feb39-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="feb39-709">SDK de Windows</span><span class="sxs-lookup"><span data-stu-id="feb39-709">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="feb39-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Directrices de control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="feb39-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="feb39-711">[Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad de control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="feb39-711">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="feb39-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Información de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="feb39-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="feb39-713">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="feb39-713">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="feb39-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portal para desarrolladores de WinQual</span><span class="sxs-lookup"><span data-stu-id="feb39-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="feb39-715">Servicios en línea de calidad de Windows (WinQual)</span><span class="sxs-lookup"><span data-stu-id="feb39-715">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="feb39-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portal para desarrolladores de DirectX</span><span class="sxs-lookup"><span data-stu-id="feb39-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="feb39-717">[Centro para desarrolladores de DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="feb39-717">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="feb39-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de juegos para Windows y DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="feb39-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="feb39-719">Juegos para Windows y el SDK de DirectX</span><span class="sxs-lookup"><span data-stu-id="feb39-719">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="feb39-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX</span><span class="sxs-lookup"><span data-stu-id="feb39-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="feb39-721">Artículos técnicos de DirectX</span><span class="sxs-lookup"><span data-stu-id="feb39-721">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

