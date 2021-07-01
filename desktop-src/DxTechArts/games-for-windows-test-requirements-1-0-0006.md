---
title: 'Casos de prueba de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan casos de prueba para juegos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120280"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="520da-103">Juegos para casos de prueba de Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8</span><span class="sxs-lookup"><span data-stu-id="520da-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="520da-104">En este artículo se proporcionan casos de prueba para juegos para Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="520da-105">Cómo usar este artículo</span><span class="sxs-lookup"><span data-stu-id="520da-105">How to Use This Article</span></span>

<span data-ttu-id="520da-106">Hay tres secciones principales para este artículo:</span><span class="sxs-lookup"><span data-stu-id="520da-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="520da-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de prueba**</span><span class="sxs-lookup"><span data-stu-id="520da-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="520da-108">Cada requisito de prueba de este documento tiene cuatro secciones principales: un título y una tabla con tres secciones importantes (columna izquierda, parte superior derecha e inferior derecha).</span><span class="sxs-lookup"><span data-stu-id="520da-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="520da-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título</span><span class="sxs-lookup"><span data-stu-id="520da-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="520da-110">Nombre del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="520da-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Cuadro, columna de extremo izquierdo</span><span class="sxs-lookup"><span data-stu-id="520da-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="520da-112">Nombres de los sistemas operativos a los que se aplica el caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="520da-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, parte superior derecha</span><span class="sxs-lookup"><span data-stu-id="520da-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="520da-114">Breve resumen del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="520da-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Cuadro, parte inferior derecha</span><span class="sxs-lookup"><span data-stu-id="520da-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="520da-116">Detalles del caso de prueba real.</span><span class="sxs-lookup"><span data-stu-id="520da-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="520da-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script de prueba de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="520da-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="520da-118">Esta sección es un ejemplo de la secuencia que seguiría una prueba típica si se usan los requisitos de prueba como guía.</span><span class="sxs-lookup"><span data-stu-id="520da-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="520da-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas de la herramienta de prueba**</span><span class="sxs-lookup"><span data-stu-id="520da-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="520da-120">Esta sección contiene notas detalladas sobre cada una de las herramientas de prueba usadas para comprobar las condiciones de superación o error en los requisitos de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="520da-121">Requisitos de prueba</span><span class="sxs-lookup"><span data-stu-id="520da-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="520da-122">1. Requisitos del juego</span><span class="sxs-lookup"><span data-stu-id="520da-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="520da-123">1.1 Explorador de juegos de Windows</span><span class="sxs-lookup"><span data-stu-id="520da-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-124">Windows 7</span></span><br/> <span data-ttu-id="520da-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-126">El juego debe estar visible en el Explorador de juegos en Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="520da-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="520da-127">Cuando se selecciona, el juego también debe mostrar los metadatos correctos.</span><span class="sxs-lookup"><span data-stu-id="520da-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="520da-128">La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="520da-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="520da-129">No se deben crear tareas ni métodos abreviados para la eliminación.</span><span class="sxs-lookup"><span data-stu-id="520da-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-130">Después de instalar el juego, abra El Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="520da-131">Compruebe que el icono del juego se muestra en el Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="520da-132">Haga clic con el botón derecho en el icono y pruebe cada reproducción definida por la & de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="520da-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="520da-133">Haga clic en el icono y compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) en la parte inferior se muestran y son correctos.</span><span class="sxs-lookup"><span data-stu-id="520da-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="520da-134">Compruebe que el icono del juego muestra información de Índice de experiencia de Windows (WEI) en El Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="520da-135">Compruebe que los hipervínculos de juegos para metadatos funcionan correctamente en El Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="520da-136">(Si los hipervínculos no se muestran, se trata de un posible signo de que el archivo exe no está firmado; vea <a href="#23-sign-files">la sección 2.3).</a></span><span class="sxs-lookup"><span data-stu-id="520da-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="520da-137">Compruebe que el juego muestra una clasificación de control parental precisa en El Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="520da-138">(Si dice no clasificado, compruebe que se trata de un juego no clasificado; de lo contrario, es un indicador de que el archivo exe no está firmado; vea la sección <a href="#23-sign-files">2.3).</a></span><span class="sxs-lookup"><span data-stu-id="520da-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="520da-139">Compruebe que el juego no coloca accesos directos de inicio en el escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="520da-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="520da-140">Haga clic en Inicio -> Todos los programas.</span><span class="sxs-lookup"><span data-stu-id="520da-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="520da-141">Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="520da-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="520da-142">Compruebe que el juego no coloca accesos directos de desinstalación en el menú Inicio fuera de Panel de control.</span><span class="sxs-lookup"><span data-stu-id="520da-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="520da-143">Si el juego se distribuye digitalmente, compruebe que el proveedor de servicios aparece en el Explorador de juegos de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="520da-144">1.2 Seguridad de la familia Windows/Controles parentales</span><span class="sxs-lookup"><span data-stu-id="520da-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-145">Windows 7</span></span><br/> <span data-ttu-id="520da-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-147">El juego debe ejecutarse en el contexto de &quot; un usuario &quot; estándar.</span><span class="sxs-lookup"><span data-stu-id="520da-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="520da-148">Los controles parentales deben poder bloquear el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="520da-149">Compruebe que GDF tiene nombres EXE.</span><span class="sxs-lookup"><span data-stu-id="520da-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-150">Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="520da-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span><span class="sxs-lookup"><span data-stu-id="520da-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="520da-152">Como Julia, desde la cuenta de administrador, configure los controles parentales para el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="520da-153">Start -> Panel de control -> Configure Parental Controls for Any User -> Toby</span><span class="sxs-lookup"><span data-stu-id="520da-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="520da-154">Compruebe que el juego se inicia desde el icono del Explorador de juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="520da-155">Compruebe que el juego muestra la clasificación de control parental precisa debajo del título del juego en el control parental Panel de control.</span><span class="sxs-lookup"><span data-stu-id="520da-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="520da-156">Antes de aplicar los controles parentales, compruebe que el juego no solicita credenciales de administrador al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="520da-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="520da-157">Establezca Controles parentales en &quot; En &quot; .</span><span class="sxs-lookup"><span data-stu-id="520da-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="520da-158">En la sección Configuración de Windows, haga clic en Juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="520da-159">Haga clic en Aceptar (la configuración ahora debe ser &quot; AO / todos los &quot; juegos).</span><span class="sxs-lookup"><span data-stu-id="520da-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="520da-160">Compruebe que el juego se ejecuta con esta configuración como User Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="520da-161">Cierre sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="520da-162">Compruebe que el juego se ejecuta con esta configuración como User Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="520da-163">Cierre sesión como Toby e inicie sesión como Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="520da-164">Vuelva a la pantalla anterior y seleccione &quot; Establecer clasificaciones de &quot; juegos.</span><span class="sxs-lookup"><span data-stu-id="520da-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="520da-165">Seleccione una clasificación inferior a la clasificación de ESRB del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-166">Si el juego no está clasificado, omita este paso y pase a la siguiente parte de esta prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="520da-167">Puede que sea necesario elegir un sistema de clasificación diferente para encontrar una clasificación de juego, en función de la configuración regional del idioma de la SKU que se está probando.</span><span class="sxs-lookup"><span data-stu-id="520da-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="520da-168">Cierre sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="520da-169">Compruebe que el juego no se inicia para El usuario Toby cuando es bloqueado por el usuario Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="520da-170">Cierre sesión como Toby e inicie sesión como Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="520da-171">Si se ha cambiado anteriormente, restaure la configuración de ESRB.</span><span class="sxs-lookup"><span data-stu-id="520da-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="520da-172">Si no hay ninguna configuración de ESRB, seleccione Bloquear o Permitir juegos específicos &quot; y seleccione el juego por &quot; nombre.</span><span class="sxs-lookup"><span data-stu-id="520da-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="520da-173">Cierre sesión como Julia e inicie sesión como Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="520da-174">Compruebe que el juego no se inicia para User Toby cuando el usuario Jane bloquea EXE/Name.</span><span class="sxs-lookup"><span data-stu-id="520da-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="520da-175">Cierre sesión como Toby y vuelva a iniciarla como Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="520da-176">Como Julia, abra Controles de usuario -> restricciones de aplicación.</span><span class="sxs-lookup"><span data-stu-id="520da-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="520da-177">Haga clic en Toby solo puede usar los programas que se permiten y haga clic en &quot; &quot; Aceptar (es decir, no permitir exes).</span><span class="sxs-lookup"><span data-stu-id="520da-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="520da-178">Vaya a Controles de usuario | Controles de juegos y permitir el juego específico mediante la clasificación de ESRB.</span><span class="sxs-lookup"><span data-stu-id="520da-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="520da-179">Cierre sesión como Julia e inicie sesión como Toby e intente jugar al juego.</span><span class="sxs-lookup"><span data-stu-id="520da-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="520da-180">Compruebe que el juego NO está bloqueado y que Toby puede reproducirlo cuando no se establece allow &quot; &quot; exes.</span><span class="sxs-lookup"><span data-stu-id="520da-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="520da-181">1.3 Juegos guardados enriquecidos de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="520da-182">Este requisito se ha retirado.</span><span class="sxs-lookup"><span data-stu-id="520da-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="520da-183">1.4 Xbox 360 controlador común para \[ requisitos condicionales de Windows\]</span><span class="sxs-lookup"><span data-stu-id="520da-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-184">Windows 7</span></span><br/> <span data-ttu-id="520da-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-185">Windows Vista</span></span><br/> <span data-ttu-id="520da-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-187">Los juegos que admiten controladores gamepad deben admitir Xbox 360 Controller para Windows mediante la API XInput.</span><span class="sxs-lookup"><span data-stu-id="520da-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="520da-188">Todas las referencias a botones y desencadenadores de controlador comunes deben usar Xbox 360 nombres.</span><span class="sxs-lookup"><span data-stu-id="520da-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-189">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-189">Launch the game.</span></span></li>
<li><span data-ttu-id="520da-190">Vaya a las opciones del controlador.</span><span class="sxs-lookup"><span data-stu-id="520da-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="520da-191">Compruebe que el juego reconoce Xbox 360 controlador para Windows como un dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="520da-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="520da-192">Jugar al juego y comprobar que el juego y el sistema de menús se pueden controlar con Xbox 360 Controller para Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="520da-193">Compruebe que el controlador Xbox 360 para Windows se comporta según los estándares aceptados.</span><span class="sxs-lookup"><span data-stu-id="520da-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="520da-194">(B para atrás, A para aceptar, Iniciar para en el menú del juego, pausar o aceptar, etc.)</span><span class="sxs-lookup"><span data-stu-id="520da-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="520da-195">Compruebe que el juego hace referencia a los botones y desencadenadores del controlador Xbox 360 nombres.</span><span class="sxs-lookup"><span data-stu-id="520da-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-196">Si el juego no admite un controlador de juego o solo admite teclado o mouse, omita este caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="520da-197">\*\* La configuración del controlador podría encontrarse fuera del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="520da-198">1.5 Varias relaciones de aspecto y resoluciones</span><span class="sxs-lookup"><span data-stu-id="520da-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-199">Windows 7</span></span><br/> <span data-ttu-id="520da-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-200">Windows Vista</span></span><br/> <span data-ttu-id="520da-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-202">El juego debe admitir al menos las siguientes relaciones de aspecto y resoluciones de pantalla asociadas:</span><span class="sxs-lookup"><span data-stu-id="520da-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="520da-203">4:3 &quot; normal &quot; (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="520da-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="520da-204">16:9 &quot; widescreen &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="520da-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="520da-205">16:10 &quot; widescreen &quot; (1152 720, 1680 1050 o 800 480)</span><span class="sxs-lookup"><span data-stu-id="520da-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-206">Busque las opciones de vídeo del juego (puede que esté fuera de juego).</span><span class="sxs-lookup"><span data-stu-id="520da-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-207">Las siguientes pruebas deben realizarse en un monitor de pantalla ancha.</span><span class="sxs-lookup"><span data-stu-id="520da-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="520da-208">En la sección de resolución de vídeo, seleccione 800 600 o 1024 768.</span><span class="sxs-lookup"><span data-stu-id="520da-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="520da-209">Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3.</span><span class="sxs-lookup"><span data-stu-id="520da-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="520da-210">En la sección de resolución de vídeo, seleccione 1280 720.</span><span class="sxs-lookup"><span data-stu-id="520da-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="520da-211">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9.</span><span class="sxs-lookup"><span data-stu-id="520da-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="520da-212">En la sección de resolución de vídeo, seleccione 1680 1050, 800 480 o 1152 720.</span><span class="sxs-lookup"><span data-stu-id="520da-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="520da-213">Compruebe que el juego se ejecuta en una resolución de relación de aspecto de 16:10.</span><span class="sxs-lookup"><span data-stu-id="520da-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="520da-214">Compruebe que el juego no extiende la imagen y, a su vez, presenta un área de vista más amplia.</span><span class="sxs-lookup"><span data-stu-id="520da-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="520da-215">Compruebe que el juego solicita al usuario cuando se realiza un cambio en la resolución.</span><span class="sxs-lookup"><span data-stu-id="520da-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="520da-216">Si el usuario no acepta en 15 segundos, compruebe que la pantalla vuelve a la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="520da-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="520da-217">Compruebe que el juego no agrega barras negras a la izquierda y derecha del área de juego.</span><span class="sxs-lookup"><span data-stu-id="520da-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="520da-218">(En este caso, verá que el área de juego sigue en una relación de 4:3 en el centro de la pantalla).</span><span class="sxs-lookup"><span data-stu-id="520da-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="520da-219">1.6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="520da-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="520da-220">Este requisito se ha retirado.</span><span class="sxs-lookup"><span data-stu-id="520da-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="520da-221">1.7 Requisito condicional de \[ Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="520da-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="520da-222">SO</span><span class="sxs-lookup"><span data-stu-id="520da-222">OS</span></span>                                                                    | <span data-ttu-id="520da-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="520da-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520da-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-224">Windows 7</span></span><br/> <span data-ttu-id="520da-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-225">Windows Vista</span></span><br/> <span data-ttu-id="520da-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-226">Windows XP</span></span><br/> | <span data-ttu-id="520da-227">Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el valor predeterminado para cualquier opción de configuración de pantalla.</span><span class="sxs-lookup"><span data-stu-id="520da-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="520da-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span><span class="sxs-lookup"><span data-stu-id="520da-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="520da-229">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-229">Launch the game.</span></span> <span data-ttu-id="520da-230">En las opciones de vídeo, compruebe si hay opciones de representación, D3D o OpenGL.</span><span class="sxs-lookup"><span data-stu-id="520da-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="520da-231">Si las hay, compruebe que las opciones de representación del juego tienen como valor predeterminado Direct3D.</span><span class="sxs-lookup"><span data-stu-id="520da-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="520da-232">Si no puede comprobar que D3D9 es la versión de DirectX que se usa, continúe con La prueba automatizada.</span><span class="sxs-lookup"><span data-stu-id="520da-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="520da-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt></span><span class="sxs-lookup"><span data-stu-id="520da-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="520da-234">Usar herramienta: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="520da-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="520da-235">1.8 Habilitar reconocimiento de valores altos de PPP</span><span class="sxs-lookup"><span data-stu-id="520da-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-236">Windows 7</span></span><br/> <span data-ttu-id="520da-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-238">Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando el escalado de PPP está habilitado.</span><span class="sxs-lookup"><span data-stu-id="520da-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="520da-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="520da-240">Establezca el sistema en PPP 150 %:</span><span class="sxs-lookup"><span data-stu-id="520da-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="520da-241">Windows Vista: Panel de control personalización, ajustar el tamaño de fuente (PPP), PPP personalizado.</span><span class="sxs-lookup"><span data-stu-id="520da-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="520da-242">Establezca en 150 %.</span><span class="sxs-lookup"><span data-stu-id="520da-242">Set to 150%.</span></span><br/> <span data-ttu-id="520da-243">Windows 7: Panel de control: Mostrar, Establecido en Mayor - 150 %.</span><span class="sxs-lookup"><span data-stu-id="520da-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="520da-244">Ejecute el proceso de instalación y el juego para comprobar que no hay ningún problema con las pantallas recortadas o los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="520da-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="520da-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="520da-246">Compruebe que el <dpiAware>elemento true</dpiAware> está contenido en el manifiesto incrustado.</span><span class="sxs-lookup"><span data-stu-id="520da-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="520da-247">Usar herramienta: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="520da-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="520da-248">2. Seguridad y compatibilidad</span><span class="sxs-lookup"><span data-stu-id="520da-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="520da-249">2.1 Siga las instrucciones de control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="520da-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-250">Windows 7</span></span><br/> <span data-ttu-id="520da-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-252">Cada archivo ejecutable (.EXE extensión) incluido con una aplicación debe tener un manifiesto incrustado que defina su nivel de ejecución:</span><span class="sxs-lookup"><span data-stu-id="520da-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-253">En el caso de los juegos y instaladores de juegos, uiAccess siempre debe establecerse en &quot; &quot; false.</span><span class="sxs-lookup"><span data-stu-id="520da-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-254">Compruebe que los archivos ejecutables del juego contienen manifiestos.</span><span class="sxs-lookup"><span data-stu-id="520da-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="520da-255">Compruebe que el manifiesto del archivo ejecutable del juego solicitadoExecutionLevel &quot; es AsInvoker. &quot;</span><span class="sxs-lookup"><span data-stu-id="520da-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="520da-256">Usar herramienta: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="520da-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="520da-257">2.2 Compatibilidad con versiones x64 de Windows</span><span class="sxs-lookup"><span data-stu-id="520da-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-258">Windows 7</span></span><br/> <span data-ttu-id="520da-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-260">Para mantener la compatibilidad con las versiones x64 de Windows:</span><span class="sxs-lookup"><span data-stu-id="520da-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="520da-261">Los títulos y los instaladores de título no deben contener ningún código de 16 bits ni depender de ningún componente de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="520da-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="520da-262">Si el juego depende de los controladores en modo kernel para el funcionamiento, las versiones x64 de estos controladores deben estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="520da-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="520da-263">La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-264">La compatibilidad con la edición de 64 bits de Windows XP Professional es opcional.</span><span class="sxs-lookup"><span data-stu-id="520da-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-265">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="520da-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="520da-266">Ejecute el juego en ediciones de 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="520da-267">Compruebe que el proceso de instalación del juego se ejecuta normalmente en ediciones de 64 bits de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="520da-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="520da-268">Compruebe que el juego no encuentra un error como resultado de archivos ejecutables de 16 bits en ediciones de 64 bits de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="520da-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="520da-269">El error mencionará la aplicación de 16 bits en la ventana de error.</span><span class="sxs-lookup"><span data-stu-id="520da-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="520da-270">Si el juego tiene un ejecutable nativo de 64 bits, úselo también.</span><span class="sxs-lookup"><span data-stu-id="520da-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="520da-271">2.3 Archivos de firma</span><span class="sxs-lookup"><span data-stu-id="520da-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-272">Windows 7</span></span><br/> <span data-ttu-id="520da-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-273">Windows Vista</span></span><br/> <span data-ttu-id="520da-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-275">Todos los archivos de código ejecutable (por ejemplo, .exe y .dll) deben estar firmados con un certificado Authenticode.</span><span class="sxs-lookup"><span data-stu-id="520da-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="520da-276">Si usa Windows Installer, los archivos de paquete del instalador (.msi archivos) deben estar firmados.</span><span class="sxs-lookup"><span data-stu-id="520da-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-277">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="520da-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="520da-278">Vaya al directorio del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="520da-279">Busque todos los archivos .exe y .dll archivos.</span><span class="sxs-lookup"><span data-stu-id="520da-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="520da-280">Haga clic con el botón derecho en Propiedades en cada archivo.</span><span class="sxs-lookup"><span data-stu-id="520da-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="520da-281">Compruebe que los archivos ejecutables del juego contienen una firma digital.</span><span class="sxs-lookup"><span data-stu-id="520da-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="520da-282">2.4 Controladores de firma</span><span class="sxs-lookup"><span data-stu-id="520da-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-283">Windows 7</span></span><br/> <span data-ttu-id="520da-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-284">Windows Vista</span></span><br/> <span data-ttu-id="520da-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-286">Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente.</span><span class="sxs-lookup"><span data-stu-id="520da-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="520da-287">Cualquier controlador de dispositivo de hardware en modo kernel instalado por el juego debe tener una firma de Microsoft obtenida a través del programa Laboratorios de calidad de hardware de Windows (WHQL) (WHQL) o firma de confiabilidad de controladores (DRS).</span><span class="sxs-lookup"><span data-stu-id="520da-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-288">Prueba manual</span><span class="sxs-lookup"><span data-stu-id="520da-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="520da-289">Instale el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-289">Install the game.</span></span></li>
<li><span data-ttu-id="520da-290">Compruebe que el proceso de instalación del juego no muestra diálogos de controladores sin signo.</span><span class="sxs-lookup"><span data-stu-id="520da-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="520da-291">2.5 Realizar correctamente la comprobación de versiones</span><span class="sxs-lookup"><span data-stu-id="520da-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-292">Windows 7</span></span><br/> <span data-ttu-id="520da-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-293">Windows Vista</span></span><br/> <span data-ttu-id="520da-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-295">Los juegos no deben dejar de ejecutarse en sistemas operativos futuros, como indican los cambios en el número de versión de Windows, a menos que el Contrato de licencia del usuario final prohíba el uso en sistemas operativos futuros.</span><span class="sxs-lookup"><span data-stu-id="520da-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="520da-296">Si se supone que se producirá un error en el juego, debe hacerlo correctamente mostrando un mensaje al usuario.</span><span class="sxs-lookup"><span data-stu-id="520da-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="520da-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="520da-298">Instale el juego en Windows XP, en ediciones de 32 bits de Windows Vista y Windows 7, y en ediciones de 64 bits de Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="520da-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="520da-299">Compruebe que el proceso de instalación del juego no encuentra un error con respecto a la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="520da-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="520da-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="520da-301">Usar herramienta: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="520da-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="520da-302">Inicie Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="520da-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="520da-303">Habilite la prueba Compatibility:HighVersionLie después de seleccionar el INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="520da-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="520da-304">Instale el juego y asegúrese de que no bloquea la instalación en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="520da-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="520da-305">Habilite la prueba Compatibility:HighVersionLie después de seleccionar el GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="520da-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="520da-306">Ejecute el juego y asegúrese de que no bloquea la ejecución en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="520da-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="520da-307">2.6 Compatibilidad con sesiones de usuario simultáneas</span><span class="sxs-lookup"><span data-stu-id="520da-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-308">Windows 7</span></span><br/> <span data-ttu-id="520da-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-309">Windows Vista</span></span><br/> <span data-ttu-id="520da-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-311">Los juegos deben admitir escenarios estándar de multitarea de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-312">Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="520da-313">Iniciar -> Panel de control -> Agregar o quitar cuentas de usuario -> Crear nueva cuenta</span><span class="sxs-lookup"><span data-stu-id="520da-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="520da-314">Inicie el juego como User Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="520da-315">ALT+TAB de vuelta al escritorio.</span><span class="sxs-lookup"><span data-stu-id="520da-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="520da-316">Compruebe que el juego se ha configurado correctamente con ALT+TAB en el escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="520da-317">Haga clic en Start -> [arrow to the right of Lock] -> Switch User (Iniciar -> [flecha a la derecha de Bloquear] -> Cambiar usuario).</span><span class="sxs-lookup"><span data-stu-id="520da-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="520da-318">Inicie sesión como User Toby.</span><span class="sxs-lookup"><span data-stu-id="520da-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="520da-319">Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="520da-320">Compruebe que el juego no encuentra errores para User Toby o User Jane durante el proceso de cambio de usuario.</span><span class="sxs-lookup"><span data-stu-id="520da-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="520da-321">Si puedes iniciar otra sesión de juego, comprueba que no puedes escuchar audio de la sesión de juego original.</span><span class="sxs-lookup"><span data-stu-id="520da-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="520da-322">Cierre el juego y vuelva al usuario y al juego originales.</span><span class="sxs-lookup"><span data-stu-id="520da-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="520da-323">2.7 Compatibilidad con nombres largos</span><span class="sxs-lookup"><span data-stu-id="520da-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-324">Windows 7</span></span><br/> <span data-ttu-id="520da-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-325">Windows Vista</span></span><br/> <span data-ttu-id="520da-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-327">Si un juego admite guardar archivos, debe ser capaz de guardar archivos que tengan nombres y rutas de acceso largos.</span><span class="sxs-lookup"><span data-stu-id="520da-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="520da-328">El juego debe controlar correctamente los caracteres especiales del sistema de archivos, como \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="520da-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="520da-329">&quot; < o > en los campos de entrada del usuario que se usan para crear rutas de acceso o nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="520da-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-330">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-330">Launch the game.</span></span></li>
<li><span data-ttu-id="520da-331">Inicie un nuevo juego.</span><span class="sxs-lookup"><span data-stu-id="520da-331">Start a new game.</span></span></li>
<li><span data-ttu-id="520da-332">Guarde el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-332">Save the game.</span></span> <span data-ttu-id="520da-333">Durante el proceso de guardado, compruebe que el juego se guarda con el nombre guardado: Mi primer juego de guardar.</span><span class="sxs-lookup"><span data-stu-id="520da-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="520da-334">Vuelva al menú principal.</span><span class="sxs-lookup"><span data-stu-id="520da-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="520da-335">Intente cargar el juego recién guardado.</span><span class="sxs-lookup"><span data-stu-id="520da-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="520da-336">Compruebe que el juego no encuentra errores al controlar los caracteres del sistema de archivos no admitidos, como \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="520da-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="520da-337">&quot; < o > Si el juego lo permite, asigne un nombre al juego guardado.</span><span class="sxs-lookup"><span data-stu-id="520da-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="520da-338">Si el usuario puede dar nombre a su perfil o carácter o guardar juegos, compruebe que el juego no encuentra errores al usar también nombres de archivo largos aquí.</span><span class="sxs-lookup"><span data-stu-id="520da-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="520da-339">3. Instalación</span><span class="sxs-lookup"><span data-stu-id="520da-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="520da-340">3.1 Instalación sencilla</span><span class="sxs-lookup"><span data-stu-id="520da-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-341">Windows 7</span></span><br/> <span data-ttu-id="520da-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-342">Windows Vista</span></span><br/> <span data-ttu-id="520da-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-344">Los juegos con una instalación tradicional deben proporcionar una ruta de acceso simplificada en su interfaz de usuario de configuración.</span><span class="sxs-lookup"><span data-stu-id="520da-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-345">Inserte el disco del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="520da-346">Compruebe que el juego no muestra más de un End-User licencia (CLUF).</span><span class="sxs-lookup"><span data-stu-id="520da-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="520da-347">Si el juego admite una opción de instalación personalizada o avanzada, compruebe que esta opción es accesible durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="520da-348">Compruebe que la opción instalación predeterminada omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, entre otras).</span><span class="sxs-lookup"><span data-stu-id="520da-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="520da-349">Compruebe que el proceso de instalación del juego no solicita la configuración del componente del sistema operativo (instalación de DirectX, entornos de ejecución de Visual C, entre otros).</span><span class="sxs-lookup"><span data-stu-id="520da-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="520da-350">Compruebe que el proceso de instalación del juego no solicita la interacción del firewall.</span><span class="sxs-lookup"><span data-stu-id="520da-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="520da-351">Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="520da-352">Compruebe que el proceso de desinstalación del juego quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra toda la configuración.</span><span class="sxs-lookup"><span data-stu-id="520da-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="520da-353">No es necesario limpiar toda la configuración y los datos por usuario (como juegos guardados).</span><span class="sxs-lookup"><span data-stu-id="520da-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="520da-354">3.2 Compatibilidad con el control de cuentas de usuario para la instalación</span><span class="sxs-lookup"><span data-stu-id="520da-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-355">Windows 7</span></span><br/> <span data-ttu-id="520da-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="520da-357">El instalador del juego no debe asumir que se ejecuta en el mismo contexto que el usuario.</span><span class="sxs-lookup"><span data-stu-id="520da-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="520da-358">Por lo tanto, los juegos deben realizar tareas por usuario en la primera ejecución por separado de la instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-359">Compruebe que puede instalar el juego como User Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="520da-360">(Esto requerirá derechos elevados durante el proceso de instalación o instalación).</span><span class="sxs-lookup"><span data-stu-id="520da-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="520da-361">Compruebe que el proceso de instalación del juego solicita al usuario Jane que eleve a través de credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="520da-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="520da-362">(La solicitud de elevación aparecerá cuando el usuario intente instalar).</span><span class="sxs-lookup"><span data-stu-id="520da-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="520da-363">Opte por ejecutar automáticamente el juego al final de la instalación, si aún no lo hace, o iniciarlo desde el menú que aparece.</span><span class="sxs-lookup"><span data-stu-id="520da-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="520da-364">Una vez en el juego, cree un nuevo perfil, jugar y guardar un juego.</span><span class="sxs-lookup"><span data-stu-id="520da-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="520da-365">Salga del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-365">Exit the game.</span></span></li>
<li><span data-ttu-id="520da-366">Reinicie el juego y compruebe que la cuenta User Jane puede acceder a los perfiles de usuario y a los juegos guardados.</span><span class="sxs-lookup"><span data-stu-id="520da-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="520da-367">3.3 Instalar en carpetas correctas</span><span class="sxs-lookup"><span data-stu-id="520da-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-368">Windows 7</span></span><br/> <span data-ttu-id="520da-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-369">Windows Vista</span></span><br/> <span data-ttu-id="520da-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-371">Los juegos deben instalarse en la carpeta Archivos de programa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="520da-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="520da-372">Los datos de usuario deben escribirse en la primera ejecución y no durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-373">Instale el juego con el tipo de instalación Predeterminado.</span><span class="sxs-lookup"><span data-stu-id="520da-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="520da-374">Compruebe que el juego se instaló en Archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="520da-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-375">Si se produce un error en esta prueba, compruebe que el juego está pensado para instalarse para Todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="520da-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="520da-376">Si es así, se trata de un error.</span><span class="sxs-lookup"><span data-stu-id="520da-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="520da-377">3.4 Instalar correctamente los recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="520da-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-378">Windows 7</span></span><br/> <span data-ttu-id="520da-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-379">Windows Vista</span></span><br/> <span data-ttu-id="520da-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-381">Las aplicaciones no deben intentar instalar archivos o claves del Registro protegidos por Protección de recursos de Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="520da-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="520da-382">Compruebe que no Protección de recursos de Windows cuadro de diálogo WRP durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="520da-383">3.5 Evitar reinicios durante la instalación</span><span class="sxs-lookup"><span data-stu-id="520da-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-384">Windows 7</span></span><br/> <span data-ttu-id="520da-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-385">Windows Vista</span></span><br/> <span data-ttu-id="520da-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-387">El instalador del juego no debe suponer que la instalación de componentes de Windows desde paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o por la documentación de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="520da-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-388">Instale el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-388">Install the game.</span></span></li>
<li><span data-ttu-id="520da-389">Compruebe que el juego no requiere que el sistema se reinicie después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-390">Si una actualización del sistema de Microsoft REDIST requiere un reinicio, haga lo siguiente: Complete la instalación del juego, desinstale el juego y vuelva a instalarlo una segunda vez.</span><span class="sxs-lookup"><span data-stu-id="520da-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="520da-391">El proceso de instalación del juego no debe requerir un reinicio en esta segunda instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="520da-392">3.6 Usar el control de versiones de archivos correctamente</span><span class="sxs-lookup"><span data-stu-id="520da-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-393">Windows 7</span></span><br/> <span data-ttu-id="520da-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-394">Windows Vista</span></span><br/> <span data-ttu-id="520da-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-396">El programa de instalación del juego debe comprobar correctamente para asegurarse de que están instaladas las versiones de archivo más recientes.</span><span class="sxs-lookup"><span data-stu-id="520da-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="520da-397">La instalación de un juego nunca debe volver a los archivos que no se producen o que comparten las aplicaciones que no se producen.</span><span class="sxs-lookup"><span data-stu-id="520da-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-398">Antes de instalar el juego, cree una instantánea previa a la instalación de System32.</span><span class="sxs-lookup"><span data-stu-id="520da-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="520da-399">Crear un directorio denominado G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="520da-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="520da-400">Abre una ventana de comandos (Start -> Run -> cmd).</span><span class="sxs-lookup"><span data-stu-id="520da-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="520da-401">Vaya a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="520da-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="520da-402">Escriba dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="520da-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="520da-403">Cree una instantánea posterior a la instalación de System32.</span><span class="sxs-lookup"><span data-stu-id="520da-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="520da-404">Abre una ventana de comandos (Start -> Run -> cmd).</span><span class="sxs-lookup"><span data-stu-id="520da-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="520da-405">Vaya a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="520da-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="520da-406">Escriba dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="520da-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="520da-407">Compruebe que el juego no revierte ninguna versión de archivo de archivos que el juego no produjo (... de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="520da-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="520da-408">3.7 Compatibilidad con el requisito condicional de ejecución \[ automática\]</span><span class="sxs-lookup"><span data-stu-id="520da-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-409">Windows 7</span></span><br/> <span data-ttu-id="520da-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-410">Windows Vista</span></span><br/> <span data-ttu-id="520da-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-412">En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admiten la ejecución automática, cuando el disco se inserta por primera vez, la aplicación debe ejecutarse automáticamente o pedir al usuario que instale el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-413">Los programas de ejecución automática que se escribieron para su uso en versiones de Windows anteriores a Windows Vista no deben usar el runtime de .NET, ya que esta tecnología no se incluye con Windows XP ni con versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="520da-414">Para obtener más instrucciones, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun (Juegos para Windows Technical Requirements 3.7, Ejecución automática de soporte técnico).</span><span class="sxs-lookup"><span data-stu-id="520da-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="520da-415">Inserte el disco o los medios del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="520da-416">Compruebe que el cuadro de diálogo instalar o ejecutar aparece automáticamente.</span><span class="sxs-lookup"><span data-stu-id="520da-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="520da-417">Windows Vista o Windows 7: compruebe que el propio programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="520da-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="520da-418">Compruebe que el ejecutable autoejecución no necesita componentes DE REDIST estándar, como .NET 3.5, bibliotecas de C Run-Time, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="520da-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="520da-419">Compruebe que volver a insertar el disco en la unidad después de la instalación no hace que la instalación se vuelva a iniciar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="520da-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="520da-420">4. Confiabilidad</span><span class="sxs-lookup"><span data-stu-id="520da-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="520da-421">4.1 Eliminar reinicios innecesarios</span><span class="sxs-lookup"><span data-stu-id="520da-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="520da-422">SO</span><span class="sxs-lookup"><span data-stu-id="520da-422">OS</span></span>                                              | <span data-ttu-id="520da-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="520da-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520da-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-424">Windows 7</span></span><br/> <span data-ttu-id="520da-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-425">Windows Vista</span></span><br/> | <span data-ttu-id="520da-426">Todos los instaladores de aplicaciones deben aprovechar las API de Restart Manager para evitar reinicios del sistema (consulte el [requisito 3.5).](#35-avoid-reboots-during-installation)</span><span class="sxs-lookup"><span data-stu-id="520da-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="520da-427">4.2 Eliminar Application Verifier errores</span><span class="sxs-lookup"><span data-stu-id="520da-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-428">Windows 7</span></span><br/> <span data-ttu-id="520da-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-429">Windows Vista</span></span><br/> <span data-ttu-id="520da-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-431">El juego no debe generar errores en ejecución en Microsoft Application Verifier (AppVerifier), versión 4.0 o posterior, en las siguientes pruebas:</span><span class="sxs-lookup"><span data-stu-id="520da-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="520da-432">Aspectos básicos: Identificadores, montones, bloqueos, memoria, TLS</span><span class="sxs-lookup"><span data-stu-id="520da-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="520da-433">Varios: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="520da-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-434">Usar herramienta: AppVerifier 4.0 (o posterior)</span><span class="sxs-lookup"><span data-stu-id="520da-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="520da-435">Instale AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="520da-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="520da-436">Inicie AppVerifier y seleccione Archivo -> Agregar aplicación.</span><span class="sxs-lookup"><span data-stu-id="520da-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="520da-437">Busque el archivo ejecutable del juego, selecciónelo y haga clic en &quot; el botón &quot; Abrir.</span><span class="sxs-lookup"><span data-stu-id="520da-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="520da-438">En la &quot; sección &quot; Aplicaciones, seleccione el archivo ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="520da-439">En la sección Pruebas, seleccione las pruebas enumeradas anteriormente en las categorías Aspectos básicos y Varios &quot; &quot; (desactive ThreadPool y &quot; &quot; &quot; &quot; TimeRollOver) y asegúrese de que todas las demás pruebas no estén seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="520da-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="520da-440">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-440">Launch the game.</span></span></li>
<li><span data-ttu-id="520da-441">Compruebe que el juego no genera errores cuando se ejecuta en Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="520da-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="520da-442">Algunas pruebas requieren que un depurador se ejecute completamente.</span><span class="sxs-lookup"><span data-stu-id="520da-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="520da-443">Esto puede requerir una versión de lanzamiento desprotegida del ejecutable del juego, ya que la tecnología antisecuencia/antisecuencia puede interferir con AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="520da-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="520da-444">4.3 Compatibilidad Informe de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="520da-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="520da-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-445">Windows 7</span></span><br/> <span data-ttu-id="520da-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-446">Windows Vista</span></span><br/> <span data-ttu-id="520da-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-448">Los juegos solo deben controlar las excepciones conocidas y esperadas, Informe de errores de Windows no deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="520da-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="520da-449">Si se inserta un error (como una infracción de acceso) en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="520da-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="520da-450">Herramienta de uso: subprocesamiento</span><span class="sxs-lookup"><span data-stu-id="520da-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="520da-451">Si la aplicación se bloquea durante las pruebas, compruebe que el juego Informe de errores de Windows correctamente y recopila datos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="520da-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
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
<td><span data-ttu-id="520da-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-452">Windows 7</span></span><br/> <span data-ttu-id="520da-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-453">Windows Vista</span></span><br/> <span data-ttu-id="520da-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-455">Todos los archivos ejecutables (por ejemplo, .exe o .dll archivos) deben contener un nombre de producto, un nombre de empresa y una versión de archivo precisos.</span><span class="sxs-lookup"><span data-stu-id="520da-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="520da-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Prueba manual:</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="520da-457">Haga clic con el botón derecho en los archivos ejecutables del juego en los medios de instalación y en los instalados en el disco duro del equipo.</span><span class="sxs-lookup"><span data-stu-id="520da-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="520da-458">Seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="520da-458">Select Properties.</span></span></li>
<li><span data-ttu-id="520da-459">Windows XP: haga clic en la <strong>pestaña</strong> Versión. Compruebe que los campos Nombre del producto, Nombre de la compañía y Versión de archivo están correctamente rellenados.</span><span class="sxs-lookup"><span data-stu-id="520da-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="520da-460">Windows Vista o Windows 7: haga clic en la <strong>pestaña</strong> Detalles. Compruebe que los campos Nombre del producto y Versión del archivo están correctamente rellenados.</span><span class="sxs-lookup"><span data-stu-id="520da-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="520da-461">El nombre de la empresa no está visible en la página de propiedades de Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="520da-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="520da-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Prueba automatizada:</dt> </span><span class="sxs-lookup"><span data-stu-id="520da-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="520da-463">Usar la herramienta de prueba de Microsoft Games for Windows; vea <a href="#64-microsoft-games-for-windows-test-tool">la sección 6.4.</a></span><span class="sxs-lookup"><span data-stu-id="520da-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
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
<td><span data-ttu-id="520da-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-464">Windows 7</span></span><br/> <span data-ttu-id="520da-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520da-465">Windows Vista</span></span><br/> <span data-ttu-id="520da-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="520da-467">La salida normal del juego no debe dar lugar a un error de excepción desconocido.</span><span class="sxs-lookup"><span data-stu-id="520da-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="520da-468">Después de jugar al juego para una sesión de juegos normal, compruebe que el juego no genera errores al salir.</span><span class="sxs-lookup"><span data-stu-id="520da-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="520da-469">5. Script de prueba de ejemplo</span><span class="sxs-lookup"><span data-stu-id="520da-469">5. Sample Test Script</span></span>

<span data-ttu-id="520da-470">Este es un ejemplo de un paso de prueba típico con los requisitos de prueba anteriores como guía.</span><span class="sxs-lookup"><span data-stu-id="520da-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="520da-471">5.1 Herramientas</span><span class="sxs-lookup"><span data-stu-id="520da-471">5.1 Tools</span></span>

-   <span data-ttu-id="520da-472">Edición de 32 bits de Windows Vista SP1 o Windows 7 en una CPU amd</span><span class="sxs-lookup"><span data-stu-id="520da-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="520da-473">Edición de 32 bits de Windows Vista SP1 o Windows 7 en una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="520da-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="520da-474">Edición de 64 bits de Windows Vista SP1 o Windows 7 en una CPU amd</span><span class="sxs-lookup"><span data-stu-id="520da-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="520da-475">Edición de 64 bits de Windows Vista SP1 o Windows 7 en una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="520da-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="520da-476">Edición de 32 bits de Windows XP SP2 en una CPU amd</span><span class="sxs-lookup"><span data-stu-id="520da-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="520da-477">Edición de 32 bits de Windows XP SP2 en una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="520da-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="520da-478">Monitor de pantalla ancha que admite 1680 1050</span><span class="sxs-lookup"><span data-stu-id="520da-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="520da-479">Xbox 360 controlador para Windows</span><span class="sxs-lookup"><span data-stu-id="520da-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="520da-480">5.2 Preinstalación</span><span class="sxs-lookup"><span data-stu-id="520da-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="520da-481">Windows Vista y Windows 7: Crear dos usuarios estándar: Jane y Toby</span><span class="sxs-lookup"><span data-stu-id="520da-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="520da-482">Windows Vista y Windows 7: asegúrese de que el control de cuentas de usuario está habilitado</span><span class="sxs-lookup"><span data-stu-id="520da-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="520da-483">Creación de una instantánea previa a la instalación de System32</span><span class="sxs-lookup"><span data-stu-id="520da-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="520da-484">Crear un directorio denominado G4Wtest</span><span class="sxs-lookup"><span data-stu-id="520da-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="520da-485">Abrir una ventana de comandos (Start -> Run -> cmd)</span><span class="sxs-lookup"><span data-stu-id="520da-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="520da-486">Vaya a c: \\ sistema \\ de Windows32</span><span class="sxs-lookup"><span data-stu-id="520da-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="520da-487">Escriba dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="520da-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="520da-488">Windows Vista y Windows 7: establecido en 150 % PPP \[ 1,8\]</span><span class="sxs-lookup"><span data-stu-id="520da-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="520da-489">Vaya a [Instalación.](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="520da-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="520da-490">5.3 Instalar</span><span class="sxs-lookup"><span data-stu-id="520da-490">5.3 Install</span></span>

1.  <span data-ttu-id="520da-491">Iniciar sesión como User Jane</span><span class="sxs-lookup"><span data-stu-id="520da-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="520da-492">Inserte el disco del juego en la unidad de CD/DVD y compruebe que el cuadro de diálogo instalar o ejecutar aparece automáticamente \[ 3.7.\]</span><span class="sxs-lookup"><span data-stu-id="520da-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="520da-493">Compruebe que el proceso de instalación del juego solicita al usuario Julia que eleve las credenciales de administrador \[ 3.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="520da-494">Compruebe que el propio programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de credenciales de administrador \[ 3.7.\]</span><span class="sxs-lookup"><span data-stu-id="520da-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="520da-495">Compruebe que el juego no muestra más de un End-User licencia (CLUF) \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="520da-496">Compruebe que el juego muestra las opciones de instalación Predeterminada, Fácil y \[ Personalizada/Avanzada 3.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="520da-497">Compruebe que la opción de instalación Predeterminada/Fácil omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, y así sucesivamente). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="520da-498">Compruebe que el proceso de instalación del juego no solicita la configuración del componente del sistema operativo (instalación de DirectX, bibliotecas de Run-Time C, y así sucesivamente). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="520da-499">Compruebe que el proceso de instalación del juego no solicita la interacción del firewall \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="520da-500">Compruebe que el proceso de instalación del juego no encuentra un error relacionado con la versión \[ 2.5 \] \[ 4.2 del sistema operativo.\]</span><span class="sxs-lookup"><span data-stu-id="520da-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="520da-501">Compruebe que el proceso de instalación del juego no muestra los cuadros de diálogo de controladores sin signo \[ 2.4.\]</span><span class="sxs-lookup"><span data-stu-id="520da-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="520da-502">Compruebe que no Protección de recursos de Windows diálogos de Protección de recursos de Windows (WRP) durante el proceso de instalación \[ 3.4\]</span><span class="sxs-lookup"><span data-stu-id="520da-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="520da-503">Compruebe que volver a insertar el disco en la unidad después de la instalación no hace que la instalación se vuelva a iniciar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="520da-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="520da-504">Compruebe que el juego no requiere que el sistema se reinicie después de la \[ instalación 3.5.\]</span><span class="sxs-lookup"><span data-stu-id="520da-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="520da-505">Compruebe que puede instalar el juego como user Jane \[ 3.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="520da-506">Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación \[ 3.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="520da-507">Si el juego se ejecuta automáticamente después de la instalación, vaya directamente a [Runtime (Tiempo de ejecución).](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="520da-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="520da-508">Si el juego dejó un menú de inicio o no se pudo desinstalar, consulte la sección [Posterior a la instalación.](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="520da-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="520da-509">5.4 Posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="520da-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="520da-510">Comprobar que el juego no coloca accesos directos de inicio en el escritorio del usuario \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="520da-511">Compruebe que el juego no coloca accesos directos de inicio en el menú \[ Inicio 1.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="520da-512">Compruebe que el icono del juego se muestra en el Explorador de juegos de Windows \[ 1.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="520da-513">Compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) en la parte inferior se muestran y es correcto \[ 1.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="520da-514">Compruebe que el icono del juego muestra información del Índice de experiencia de Windows (WEI) en el Explorador de juegos de Windows \[ 1.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="520da-515">Compruebe que los hipervínculos de juegos para metadatos funcionan correctamente en el Explorador de juegos de Windows \[ 1.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="520da-516">Comprobación de que el juego muestra una clasificación de control parental precisa en el Explorador de juegos de Windows \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="520da-517">Creación de una instantánea posterior a la instalación de System32</span><span class="sxs-lookup"><span data-stu-id="520da-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="520da-518">Abrir una ventana de comandos (Start -> Run -> cmd)</span><span class="sxs-lookup"><span data-stu-id="520da-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="520da-519">Vaya a c: \\ sistema \\ de Windows32</span><span class="sxs-lookup"><span data-stu-id="520da-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="520da-520">Escriba dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="520da-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="520da-521">Compruebe que el juego no revierte ninguna versión de archivo de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt \[ 3.6\]</span><span class="sxs-lookup"><span data-stu-id="520da-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="520da-522">Continúe [con](#55-runtime) runtime</span><span class="sxs-lookup"><span data-stu-id="520da-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="520da-523">5.5 Runtime</span><span class="sxs-lookup"><span data-stu-id="520da-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="520da-524">RUNTIME 1: si el menú de inicio está presente, inicie el juego desde allí.</span><span class="sxs-lookup"><span data-stu-id="520da-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="520da-525">Si el juego se ejecutó automáticamente o se inició desde el menú del iniciador del juego después de la instalación, realice lo siguiente: Si no es así, vaya a RUNTIME 2:</span><span class="sxs-lookup"><span data-stu-id="520da-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="520da-526">Crear un perfil (si el juego lo permite)</span><span class="sxs-lookup"><span data-stu-id="520da-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="520da-527">Inicio de un nuevo juego</span><span class="sxs-lookup"><span data-stu-id="520da-527">Start a new game</span></span>
    3.  <span data-ttu-id="520da-528">Guardar el juego</span><span class="sxs-lookup"><span data-stu-id="520da-528">Save the game</span></span>
    4.  <span data-ttu-id="520da-529">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="520da-529">Exit the game</span></span>
    5.  <span data-ttu-id="520da-530">Inicio del juego desde Games Explorer</span><span class="sxs-lookup"><span data-stu-id="520da-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="520da-531">Compruebe que el juego se inicia desde el icono 1.2 del Explorador de \[ juegos.\]</span><span class="sxs-lookup"><span data-stu-id="520da-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="520da-532">Compruebe que el juego no solicita credenciales de administrador al iniciar \[ la versión 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="520da-533">Compruebe que se puede acceder a los perfiles de usuario y guardar juegos mediante la cuenta \[ 3.2 de User Jane.\]</span><span class="sxs-lookup"><span data-stu-id="520da-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="520da-534">Continúe con RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="520da-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="520da-535">RUNTIME 2: si el juego no se ha ejecutado automáticamente ni ha mostrado un lanzamiento desde el menú del iniciador del juego, se trata de un error de \[ 3.1; sin embargo, las pruebas pueden continuar \] normalmente:</span><span class="sxs-lookup"><span data-stu-id="520da-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="520da-536">Inicio del juego desde Games Explorer</span><span class="sxs-lookup"><span data-stu-id="520da-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="520da-537">Compruebe que el juego se inicia desde el icono 1.2 del Explorador de \[ juegos.\]</span><span class="sxs-lookup"><span data-stu-id="520da-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="520da-538">Compruebe que el juego no solicita credenciales de administrador al iniciar \[ la versión 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="520da-539">Continúe con RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="520da-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="520da-540">RUNTIME 3: si el juego admite un panel de juego, compruebe que el juego reconoce Xbox 360 Controller para Windows como un dispositivo de entrada \[ 1.4.\]</span><span class="sxs-lookup"><span data-stu-id="520da-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="520da-541">Si es necesario, habilite el controlador a través del menú de opciones.</span><span class="sxs-lookup"><span data-stu-id="520da-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="520da-542">Compruebe que el juego hace referencia a los botones y desencadenadores del controlador Xbox 360 nombres.</span><span class="sxs-lookup"><span data-stu-id="520da-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="520da-543">Compruebe que el juego y el sistema de menús se pueden controlar con Xbox 360 Controller para Windows.</span><span class="sxs-lookup"><span data-stu-id="520da-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="520da-544">Compruebe que el controlador Xbox 360 para Windows se comporta según los estándares aceptados.</span><span class="sxs-lookup"><span data-stu-id="520da-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="520da-545">Establezca el vídeo en \[ 1.5 \] :</span><span class="sxs-lookup"><span data-stu-id="520da-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="520da-546">Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3 (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="520da-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="520da-547">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9 (1280 720)</span><span class="sxs-lookup"><span data-stu-id="520da-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="520da-548">Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:10 (1680 1050, 800 480 o 1152 720).</span><span class="sxs-lookup"><span data-stu-id="520da-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="520da-549">Compruebe que el juego solicita al usuario cuando se realiza un cambio en la resolución.</span><span class="sxs-lookup"><span data-stu-id="520da-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="520da-550">Compruebe que la pantalla vuelve a la configuración anterior si no acepta en 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="520da-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="520da-551">Compruebe que el juego no extiende la imagen y, a su vez, presenta un área de vista más amplia.</span><span class="sxs-lookup"><span data-stu-id="520da-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="520da-552">Compruebe que el juego no agrega barras negras a la izquierda y derecha del área de juego.</span><span class="sxs-lookup"><span data-stu-id="520da-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="520da-553">Si está disponible en la configuración del vídeo, compruebe que las opciones de representación del juego tienen como valor predeterminado Direct3D \[ 1.7; de lo contrario, continúe \] con [Pruebas automatizadas.](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="520da-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="520da-554">Si se le solicita o si la opción está disponible, cree un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="520da-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="520da-555">Comprobar que el juego no encuentra errores al usar nombres de archivo \[ largos 2.7\]</span><span class="sxs-lookup"><span data-stu-id="520da-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="520da-556">Iniciar un juego nuevo, crear un juego guardado y comprobar que el juego no encuentra errores al controlar los caracteres del sistema de archivos \[ no admitidos 2.7\]</span><span class="sxs-lookup"><span data-stu-id="520da-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="520da-557">Compruebe que el juego se ha configurado correctamente con ALT+TAB en el escritorio de Windows \[ 2.6.\]</span><span class="sxs-lookup"><span data-stu-id="520da-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="520da-558">Cambiar usuarios con el juego en ejecución haciendo clic en Iniciar -> Cambiar usuario</span><span class="sxs-lookup"><span data-stu-id="520da-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="520da-559">Iniciar sesión como Toby</span><span class="sxs-lookup"><span data-stu-id="520da-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="520da-560">Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane \[ 2.6.\]</span><span class="sxs-lookup"><span data-stu-id="520da-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="520da-561">Compruebe que el juego no encuentra errores para User Toby o User Jane durante el proceso de cambio de usuario \[ 2.6.\]</span><span class="sxs-lookup"><span data-stu-id="520da-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="520da-562">Compruebe que no puede escuchar audio de la sesión de juego original \[ 2.6.\]</span><span class="sxs-lookup"><span data-stu-id="520da-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="520da-563">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="520da-563">Exit the game</span></span>
    7.  <span data-ttu-id="520da-564">Cerrar sesión en Toby</span><span class="sxs-lookup"><span data-stu-id="520da-564">Log off Toby</span></span>
    8.  <span data-ttu-id="520da-565">Volver al usuario original donde se ejecuta el juego</span><span class="sxs-lookup"><span data-stu-id="520da-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="520da-566">ALT+TAB de nuevo en el juego</span><span class="sxs-lookup"><span data-stu-id="520da-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="520da-567">Salir del juego</span><span class="sxs-lookup"><span data-stu-id="520da-567">Exit the game</span></span>
10. <span data-ttu-id="520da-568">Vaya a [Post-Runtime](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="520da-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="520da-569">5.6 Post-Runtime</span><span class="sxs-lookup"><span data-stu-id="520da-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="520da-570">Compruebe que el juego no genera errores al salir \[ de la versión 4.3.\]</span><span class="sxs-lookup"><span data-stu-id="520da-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="520da-571">Compruebe que el juego está instalado en Archivos de \[ programa 3.3.\]</span><span class="sxs-lookup"><span data-stu-id="520da-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="520da-572">Continúe con los [controles parentales.](/windows)</span><span class="sxs-lookup"><span data-stu-id="520da-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="520da-573">5.7 Controles parentales</span><span class="sxs-lookup"><span data-stu-id="520da-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="520da-574">Abrir controles parentales en Panel de control</span><span class="sxs-lookup"><span data-stu-id="520da-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="520da-575">Compruebe que el juego muestra la clasificación de control parental precisa debajo del título del juego en Control parental Panel de control \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="520da-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="520da-576">Consulte Caso de \[ prueba 1.2 \] para ver las pruebas siguientes:</span><span class="sxs-lookup"><span data-stu-id="520da-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="520da-577">Después de establecer Controles parentales en "On", compruebe que el juego se ejecuta con esta configuración como User Jane \[ 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="520da-578">Cerrar sesión e iniciar sesión como Toby</span><span class="sxs-lookup"><span data-stu-id="520da-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="520da-579">Compruebe que el juego se ejecuta con esta configuración como User Toby \[ 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="520da-580">Cierre la sesión e inicie sesión como Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="520da-581">En la sección Control parental, bloquee al usuario Toby para que no vea juegos de un nivel superior de ESRB desde el juego que acaba de instalar.</span><span class="sxs-lookup"><span data-stu-id="520da-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="520da-582">Ejemplo: si el juego tiene la clasificación E, estabbúla para que Toby solo pueda jugar juegos que estén clasificados como C.</span><span class="sxs-lookup"><span data-stu-id="520da-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="520da-583">Compruebe que el juego se ejecuta con esta configuración como User Jane \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="520da-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="520da-584">Cierre la sesión e inicie sesión como usuario toby</span><span class="sxs-lookup"><span data-stu-id="520da-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="520da-585">Compruebe que el juego no se inicia en User Toby cuando la aplicación ESRB está bloqueada por la usuario Jane \[ 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="520da-586">Cierre la sesión como usuario Toby y vuelva a iniciarla como usuario Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="520da-587">Si se ha cambiado anteriormente, restaure la configuración de ESRB.</span><span class="sxs-lookup"><span data-stu-id="520da-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="520da-588">Si no hay ninguna configuración de ESRB, seleccione "Bloquear o permitir juegos específicos" y seleccione el juego por nombre.</span><span class="sxs-lookup"><span data-stu-id="520da-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="520da-589">Cierre sesión como Julia y en Toby</span><span class="sxs-lookup"><span data-stu-id="520da-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="520da-590">Compruebe que el juego no se inicia en User Toby cuando la aplicación EXE/Name está bloqueada por la usuario Jane \[ 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="520da-591">Cierre sesión como Toby y vuelva a iniciarla como Julia.</span><span class="sxs-lookup"><span data-stu-id="520da-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="520da-592">Como Julia, abra Controles de usuario -> restricciones de aplicación</span><span class="sxs-lookup"><span data-stu-id="520da-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="520da-593">Haga clic en "Toby solo puede usar los programas que se permiten" y, a continuación, haga clic en Aceptar (es decir, no permitir exes)</span><span class="sxs-lookup"><span data-stu-id="520da-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="520da-594">Haga clic en la casilla Desactivar todo y, a continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="520da-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="520da-595">Vaya a Controles de usuario \| Controles de juegos y permita el juego específico mediante la clasificación de ESRB.</span><span class="sxs-lookup"><span data-stu-id="520da-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="520da-596">Cierre sesión como Julia e inicie sesión como Toby e intente jugar al juego.</span><span class="sxs-lookup"><span data-stu-id="520da-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="520da-597">Compruebe que el juego NO está bloqueado y que Toby puede reproducirlo cuando "allow no exes" está establecido \[ en 1.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="520da-598">Cierre la sesión como usuario Toby y vuelva a iniciarla como usuario Jane.</span><span class="sxs-lookup"><span data-stu-id="520da-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="520da-599">Vaya a Controles parentales en Panel de control quitar las restricciones.</span><span class="sxs-lookup"><span data-stu-id="520da-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="520da-600">Compruebe que ambos usuarios ahora pueden jugar al juego.</span><span class="sxs-lookup"><span data-stu-id="520da-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="520da-601">Continuar con las [pruebas automatizadas](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="520da-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="520da-602">5.8 Pruebas automatizadas</span><span class="sxs-lookup"><span data-stu-id="520da-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="520da-603">Compruebe que el juego no genera errores cuando se ejecuta en Application Verifier: consulte la documentación de la herramienta de prueba de marca \[ 4.2.\]</span><span class="sxs-lookup"><span data-stu-id="520da-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="520da-604">Compruebe que los archivos ejecutables del juego contienen manifiestos; consulte la documentación de la herramienta de prueba de marca \[ 2.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="520da-605">Compruebe que el manifiesto del archivo ejecutable del juego solicitadoExecutionLevel es "AsInvoker". Consulte la documentación de la herramienta de prueba de marca \[ 2.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="520da-606">Continuar con [otras pruebas](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="520da-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="520da-607">5.9 Otras pruebas</span><span class="sxs-lookup"><span data-stu-id="520da-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="520da-608">Compruebe que los archivos ejecutables del juego contienen una firma digital \[ 2.3.\]</span><span class="sxs-lookup"><span data-stu-id="520da-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="520da-609">Compruebe que el proceso de instalación del juego se ejecuta normalmente en ediciones de 64 bits de Windows Vista o Windows 7 \[ 2.3.\]</span><span class="sxs-lookup"><span data-stu-id="520da-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="520da-610">Compruebe que el juego no encuentra un error como resultado de archivos ejecutables de 16 bits en ediciones de 64 bits de Windows Vista o Windows 7 \[ 2.3\]</span><span class="sxs-lookup"><span data-stu-id="520da-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="520da-611">Forzar el bloqueo de la aplicación durante las pruebas y comprobar que el juego Informe de errores de Windows correctamente y recopila datos de bloqueo \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="520da-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="520da-612">Asegúrese de que los resúmenes de archivos \[ son correctos 4.3\]</span><span class="sxs-lookup"><span data-stu-id="520da-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="520da-613">Haga clic en Iniciar -> equipo</span><span class="sxs-lookup"><span data-stu-id="520da-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="520da-614">Vaya al directorio del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="520da-615">En la ventana de búsqueda, \* escriba.dll</span><span class="sxs-lookup"><span data-stu-id="520da-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="520da-616">Para cada archivo: haga clic con el botón derecho en el archivo y haga clic en Propiedades.</span><span class="sxs-lookup"><span data-stu-id="520da-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="520da-617">En Windows XP: haga clic en la pestaña Versión. Compruebe que los campos Nombre del producto, Nombre de la empresa y Versión de archivo están correctamente rellenados.</span><span class="sxs-lookup"><span data-stu-id="520da-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="520da-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="520da-618">\[4.3\]</span></span>
        -   <span data-ttu-id="520da-619">En Windows Vista y Windows 7: haga clic en la pestaña Detalles. Compruebe que los campos Nombre del producto y Versión del archivo están correctamente rellenados.</span><span class="sxs-lookup"><span data-stu-id="520da-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="520da-620">El nombre de la empresa no está visible en la página de propiedades de Windows Vista o Windows 7 \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="520da-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="520da-621">Repita esta comprobación para los .exe archivos</span><span class="sxs-lookup"><span data-stu-id="520da-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="520da-622">Inicie el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-622">Launch the game.</span></span>

    1.  <span data-ttu-id="520da-623">Presione CTRL+ALT+SUPR.</span><span class="sxs-lookup"><span data-stu-id="520da-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="520da-624">Haga clic en la flecha "Opciones de apagado".</span><span class="sxs-lookup"><span data-stu-id="520da-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="520da-625">Haga clic en Reiniciar.</span><span class="sxs-lookup"><span data-stu-id="520da-625">Click Restart</span></span>
    4.  <span data-ttu-id="520da-626">Comprobar que el juego no bloquea el apagado \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="520da-627">Continuar con la [desinstalación](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="520da-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="520da-628">5.10 Desinstalar</span><span class="sxs-lookup"><span data-stu-id="520da-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="520da-629">Compruebe que el proceso de desinstalación del juego quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra toda la configuración \[ 3.1.\]</span><span class="sxs-lookup"><span data-stu-id="520da-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="520da-630">Compruebe en Windows Vista o Windows 7 que Panel de control es la única manera de quitar el programa \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="520da-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="520da-631">Notas de la herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="520da-631">Test Tool Notes</span></span>

<span data-ttu-id="520da-632">Estas son notas para cada una de las herramientas de prueba enumeradas en los requisitos de prueba anteriores.</span><span class="sxs-lookup"><span data-stu-id="520da-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="520da-633">6.1 Appverifier 4.0 (o superior)</span><span class="sxs-lookup"><span data-stu-id="520da-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="520da-634">**Caso de prueba: 2.5, 4.2**</span><span class="sxs-lookup"><span data-stu-id="520da-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="520da-635">Algunas aplicaciones no se pueden ejecutar con AppVerifier en ejecución debido a la protección de copia.</span><span class="sxs-lookup"><span data-stu-id="520da-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="520da-636">Esto se puede resolver ejecutando con una versión de lanzamiento no protegida del ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="520da-637">Instalación de AppVerifier 4.0 (o posterior) en un equipo que ejecuta Windows XP</span><span class="sxs-lookup"><span data-stu-id="520da-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="520da-638">Inicie AppVerifier y haga clic en Archivo -> Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="520da-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="520da-639">Busque el archivo ejecutable del juego, selecciónelo y haga clic en Abrir.</span><span class="sxs-lookup"><span data-stu-id="520da-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="520da-640">En la sección "Aplicaciones", seleccione el ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="520da-641">Seleccione las siguientes pruebas en la sección "Aspectos básicos":</span><span class="sxs-lookup"><span data-stu-id="520da-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="520da-642">Asas</span><span class="sxs-lookup"><span data-stu-id="520da-642">Handles</span></span>
    -   <span data-ttu-id="520da-643">Montones</span><span class="sxs-lookup"><span data-stu-id="520da-643">Heaps</span></span>
    -   <span data-ttu-id="520da-644">Bloqueos</span><span class="sxs-lookup"><span data-stu-id="520da-644">Locks</span></span>
    -   <span data-ttu-id="520da-645">Memoria</span><span class="sxs-lookup"><span data-stu-id="520da-645">Memory</span></span>
    -   <span data-ttu-id="520da-646">TLS</span><span class="sxs-lookup"><span data-stu-id="520da-646">TLS</span></span>

6.  <span data-ttu-id="520da-647">Seleccione las siguientes pruebas en la sección "Varios":</span><span class="sxs-lookup"><span data-stu-id="520da-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="520da-648">Api peligrosas</span><span class="sxs-lookup"><span data-stu-id="520da-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="520da-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="520da-649">DirtyStacks</span></span>

7.  <span data-ttu-id="520da-650">Asegúrese de que todas las demás pruebas no están seleccionadas</span><span class="sxs-lookup"><span data-stu-id="520da-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="520da-651">Inicio del juego</span><span class="sxs-lookup"><span data-stu-id="520da-651">Launch the game</span></span>
9.  <span data-ttu-id="520da-652">Juego</span><span class="sxs-lookup"><span data-stu-id="520da-652">Play the game</span></span>
10. <span data-ttu-id="520da-653">Cerrar el juego</span><span class="sxs-lookup"><span data-stu-id="520da-653">Close the game</span></span>
11. <span data-ttu-id="520da-654">En AppVerifier, seleccione Ver -> registros.</span><span class="sxs-lookup"><span data-stu-id="520da-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="520da-655">En la sección "Aplicaciones", seleccione el archivo de .exe aplicación.</span><span class="sxs-lookup"><span data-stu-id="520da-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="520da-656">En la sección "Registros", seleccione el archivo de registro y observe el recuento de errores.</span><span class="sxs-lookup"><span data-stu-id="520da-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="520da-657">Si no hay errores, finalice las pruebas de AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="520da-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="520da-658">Si hay errores, haga clic en el botón Ver.</span><span class="sxs-lookup"><span data-stu-id="520da-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="520da-659">Busque en el documento (CTRL+F) gravedad="Error</span><span class="sxs-lookup"><span data-stu-id="520da-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="520da-660">Creación de errores basados en la parte LayerName= del error</span><span class="sxs-lookup"><span data-stu-id="520da-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="520da-661">6.2 Prueba de manifiesto: mt.exe</span><span class="sxs-lookup"><span data-stu-id="520da-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="520da-662">**Caso de prueba: 1.8, 2.1**</span><span class="sxs-lookup"><span data-stu-id="520da-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="520da-663">Esta herramienta se ejecuta desde un símbolo del sistema MT.exe se encuentra.</span><span class="sxs-lookup"><span data-stu-id="520da-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="520da-664">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="520da-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="520da-665">Haga clic en Inicio -> Ejecutar -> escriba cmd y haga clic en el botón Aceptar.</span><span class="sxs-lookup"><span data-stu-id="520da-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="520da-666">Ejecute la herramienta mt.exe para generar un archivo .manifest para cada archivo .exe que se instala con el juego.</span><span class="sxs-lookup"><span data-stu-id="520da-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="520da-667">Abrir el archivo .manifest generado</span><span class="sxs-lookup"><span data-stu-id="520da-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="520da-668">Asegúrese de que .exe archivo contiene lo siguiente (solicitado:</span><span class="sxs-lookup"><span data-stu-id="520da-668">Ensure that each .exe file contains the following (requested:</span></span>

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
> <span data-ttu-id="520da-669">El nivel de ejecución solicitado debe estar presente para cada archivo y pppAware debe estar presente para al menos el archivo ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="520da-670">6.3 Subprocesos de insocuos: threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="520da-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="520da-671">Esta herramienta se ejecuta desde un símbolo del sistema threadhijacker.exe se encuentra.</span><span class="sxs-lookup"><span data-stu-id="520da-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="520da-672">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="520da-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="520da-673">Donde str es el nombre \_ de \_program.exe</span><span class="sxs-lookup"><span data-stu-id="520da-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="520da-674">En Administrador de tareas, haga clic en la pestaña Procesos y busque el nombre del ejecutable del juego.</span><span class="sxs-lookup"><span data-stu-id="520da-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="520da-675">Abrir un símbolo del sistema en modo de administración</span><span class="sxs-lookup"><span data-stu-id="520da-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="520da-676">Vaya al directorio donde se encuentra threadhijacker.exe.</span><span class="sxs-lookup"><span data-stu-id="520da-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="520da-677">Tipo: **threadhijacker.exe /process:** str, donde str es el nombre del ejecutable al que desea alcanzar</span><span class="sxs-lookup"><span data-stu-id="520da-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="520da-678">6.4 Microsoft Games for Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="520da-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="520da-679">Esta herramienta se encuentra en el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="520da-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="520da-680">Una vez instalado el SDK en un equipo, el instalador de la herramienta de prueba de Games for Windows se puede colocar en el equipo de prueba e instalar.</span><span class="sxs-lookup"><span data-stu-id="520da-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="520da-681">Busque el instalador de Microsoft Games for Windows Test Tool en el equipo de desarrollo donde está instalado el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="520da-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="520da-682">De forma predeterminada, se coloca en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="520da-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="520da-683">Copie el instalador (MicrosoftGFWTestTool.msi /setup.exe) en el equipo de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="520da-684">Ejecute al programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="520da-684">Run the installer.</span></span>
3.  <span data-ttu-id="520da-685">Inicie Microsoft Games for Windows Test Tool.</span><span class="sxs-lookup"><span data-stu-id="520da-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="520da-686">En el **campo Lista de proyectos,** reemplace **Crear nuevo proyecto** por el nombre del título y haga clic en **Crear nuevo.**</span><span class="sxs-lookup"><span data-stu-id="520da-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="520da-687">Espere a que se complete la línea de base.</span><span class="sxs-lookup"><span data-stu-id="520da-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="520da-688">Rellene cualquier información que pueda tener en la **sección** Información del juego y haga clic en Actualizar información **del juego.**</span><span class="sxs-lookup"><span data-stu-id="520da-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="520da-689">Haga clic en **la pestaña Casos de** prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="520da-690">A partir de la parte superior, continúe con los casos de prueba, haciendo clic en **Pasar** o **En caso de error** según corresponda.</span><span class="sxs-lookup"><span data-stu-id="520da-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="520da-691">Vea "Escribir un error", más adelante en esta sección, para obtener más información sobre cómo incluir un error en el informe.</span><span class="sxs-lookup"><span data-stu-id="520da-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="520da-692">Vuelva a la **pestaña Proyectos** después de revisar el informe (comprobando las **pestañas** Informe y **Edición de** errores).</span><span class="sxs-lookup"><span data-stu-id="520da-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="520da-693">Haga clic **en Compilar informe.**</span><span class="sxs-lookup"><span data-stu-id="520da-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="520da-694">Se abrirá una ventana cuando finalice la compilación del informe.</span><span class="sxs-lookup"><span data-stu-id="520da-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="520da-695">Aquí encontrará un nombre de .ZIP nombrede *proyecto* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="520da-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="520da-696">Este archivo contiene todos los registros y resultados recopilados durante la fase de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="520da-697">Escribir un error</span><span class="sxs-lookup"><span data-stu-id="520da-697">Writing a Bug</span></span>

<span data-ttu-id="520da-698">Hay dos maneras de escribir un informe de errores:  puede pasar por los casos de  prueba y hacer clic en Error cuando se produce un error en el título de un caso de prueba, o bien puede hacer clic en la pestaña Edición de errores y agregar manualmente un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="520da-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="520da-699">Hacer clic en Error en un caso de prueba</span><span class="sxs-lookup"><span data-stu-id="520da-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="520da-700">Al hacer clic en **Error** en un caso de prueba, **la** lista desplegable Tipo de problema se establecerá automáticamente en el tipo de caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="520da-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="520da-701">Agregue una breve descripción al **campo Título** que describa brevemente el problema.</span><span class="sxs-lookup"><span data-stu-id="520da-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="520da-702">Agregue una descripción detallada del problema al **campo Comportamiento** observado.</span><span class="sxs-lookup"><span data-stu-id="520da-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="520da-703">Según corresponda, agregue lo que se esperaba (en lugar de una descripción del problema) al **campo Comportamiento** esperado.</span><span class="sxs-lookup"><span data-stu-id="520da-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="520da-704">Agregue una descripción detallada de cómo reproducir el problema en el **campo Repro-Steps (Pasos de** reproducción).</span><span class="sxs-lookup"><span data-stu-id="520da-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="520da-705">Cuando haya terminado, haga clic en **el botón** Guardar.</span><span class="sxs-lookup"><span data-stu-id="520da-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="520da-706">Agregar manualmente un error</span><span class="sxs-lookup"><span data-stu-id="520da-706">Manually Adding a Bug</span></span>

<span data-ttu-id="520da-707">Este proceso es el mismo que al hacer clic en **Error**, a excepción de la lista desplegable rellenada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="520da-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="520da-708">En este caso, seleccione el tipo de error de TCR adecuado o seleccione **\* \* Non-TR Issue \* \*** for bugs that fall outside of the TR range but should still be reported (Problema no TR para errores que se encuentran fuera del intervalo TR pero que todavía deben ser notificados).</span><span class="sxs-lookup"><span data-stu-id="520da-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="520da-709">Recursos</span><span class="sxs-lookup"><span data-stu-id="520da-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="520da-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Juegos para Windows: Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="520da-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="520da-711">Requisitos técnicos de Juegos para Windows: Procedimientos recomendados para juegos en Windows XP, Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="520da-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="520da-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="520da-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="520da-713">SDK de Windows</span><span class="sxs-lookup"><span data-stu-id="520da-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="520da-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Instrucciones de control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="520da-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="520da-715">[Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad con el control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="520da-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="520da-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer información</span><span class="sxs-lookup"><span data-stu-id="520da-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="520da-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="520da-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="520da-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Portal para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="520da-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="520da-719">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="520da-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="520da-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Portal para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="520da-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="520da-721">[Centro para desarrolladores de DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="520da-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="520da-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog del SDK de Juegos para Windows y DirectX</span><span class="sxs-lookup"><span data-stu-id="520da-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="520da-723">Juegos para Windows y el SDK de DirectX</span><span class="sxs-lookup"><span data-stu-id="520da-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="520da-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX</span><span class="sxs-lookup"><span data-stu-id="520da-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="520da-725">Artículos técnicos de DirectX</span><span class="sxs-lookup"><span data-stu-id="520da-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

