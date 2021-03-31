---
title: Operaciones de StoClien
description: En el ejemplo StoClien se muestra cómo el cliente usa el almacenamiento estructurado. A continuación se resumen las operaciones de StoClien.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Operaciones de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792951"
---
# <a name="stoclien-operations"></a><span data-ttu-id="1540c-105">Operaciones de StoClien</span><span class="sxs-lookup"><span data-stu-id="1540c-105">StoClien Operations</span></span>

<span data-ttu-id="1540c-106">En el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) se muestra cómo el cliente usa el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="1540c-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="1540c-107">A continuación se resumen las operaciones de StoClien.</span><span class="sxs-lookup"><span data-stu-id="1540c-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="1540c-108">El área de cliente de la ventana de la aplicación [StoClien](structured-storage-client-sample--stoclien-.md) se usa para la presentación visual del dibujo de forma libre creado con un mouse o un dispositivo de tableta.</span><span class="sxs-lookup"><span data-stu-id="1540c-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="1540c-109">Para dibujar con el mouse, mantenga presionado el botón primario del mouse mientras mueve el mouse.</span><span class="sxs-lookup"><span data-stu-id="1540c-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="1540c-110">Al soltar el botón primario del mouse finaliza el dibujo de una línea.</span><span class="sxs-lookup"><span data-stu-id="1540c-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="1540c-111">A continuación se muestra un resumen de las operaciones desde el punto de vista de Stoclien.exe como un cliente COM de la Stoserve.dll servidor COM:</span><span class="sxs-lookup"><span data-stu-id="1540c-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="1540c-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Archivo/abrir</span><span class="sxs-lookup"><span data-stu-id="1540c-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="1540c-113">Muestra el cuadro de diálogo abrir para obtener un nombre y una ruta de acceso de un archivo de dibujo de papel existente para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="1540c-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="1540c-114">Valor predeterminado. Se supone la extensión de nombre de archivo PAP para estos archivos.</span><span class="sxs-lookup"><span data-stu-id="1540c-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="1540c-115">Si se realizaron cambios en el dibujo existente cuando se elige este elemento de menú, se mostrará un cuadro de diálogo independiente en el que se preguntará al usuario si el dibujo actual debe guardarse en su archivo compuesto asociado.</span><span class="sxs-lookup"><span data-stu-id="1540c-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Archivo/guardar</span><span class="sxs-lookup"><span data-stu-id="1540c-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="1540c-117">Guarda el dibujo actual en su archivo compuesto asociado.</span><span class="sxs-lookup"><span data-stu-id="1540c-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Archivo/guardar como</span><span class="sxs-lookup"><span data-stu-id="1540c-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="1540c-119">Muestra el cuadro de diálogo Guardar como para obtener el nombre y la ruta de acceso de un nuevo archivo de dibujo de papel que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="1540c-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="1540c-120">El dibujo actual se convierte en el contenido guardado del nuevo archivo y el nuevo archivo se convierte en el nuevo archivo compuesto asociado para el dibujo.</span><span class="sxs-lookup"><span data-stu-id="1540c-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Archivo/salir</span><span class="sxs-lookup"><span data-stu-id="1540c-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="1540c-122">Sale de [StoClien](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="1540c-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1540c-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Dibujar y dibujar en</span><span class="sxs-lookup"><span data-stu-id="1540c-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="1540c-124">Activa el dibujo entre el cliente de [StoClien](structured-storage-client-sample--stoclien-.md) y el objeto de copaper del servidor.</span><span class="sxs-lookup"><span data-stu-id="1540c-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="1540c-125">Este comando bloquea el objeto de copapeles para que lo use exclusivamente este cliente y evita que otros clientes tengan acceso a la misma instancia de copaper en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1540c-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Dibujo/dibujo desactivado</span><span class="sxs-lookup"><span data-stu-id="1540c-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="1540c-127">Desactiva el dibujo entre el cliente de [StoClien](structured-storage-client-sample--stoclien-.md) y el objeto de copaper del servidor.</span><span class="sxs-lookup"><span data-stu-id="1540c-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="1540c-128">Este comando desbloquea el copapel para que este cliente lo use exclusivamente y permite que otros clientes tengan acceso a la misma instancia de copaper en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1540c-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Dibujar o volver a dibujar</span><span class="sxs-lookup"><span data-stu-id="1540c-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="1540c-130">Vuelve a dibujar en el cliente los datos de dibujo actuales contenidos en el objeto de copaper del servidor.</span><span class="sxs-lookup"><span data-stu-id="1540c-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Dibujar o borrar</span><span class="sxs-lookup"><span data-stu-id="1540c-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="1540c-132">Borra el contenido del dibujo actual y borra la imagen de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1540c-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="1540c-133">Selección de menú: lápiz/color muestra el cuadro de diálogo elegir color para obtener un nuevo color de lápiz para dibujar.</span><span class="sxs-lookup"><span data-stu-id="1540c-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Bolígrafo/medio</span><span class="sxs-lookup"><span data-stu-id="1540c-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="1540c-135">Elige el ancho medio del dibujo.</span><span class="sxs-lookup"><span data-stu-id="1540c-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="1540c-136">Una marca de verificación en esta opción de menú indica que Medium es el ancho actual del lápiz.</span><span class="sxs-lookup"><span data-stu-id="1540c-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Lápiz/grueso</span><span class="sxs-lookup"><span data-stu-id="1540c-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="1540c-138">Elige el ancho grueso del dibujo.</span><span class="sxs-lookup"><span data-stu-id="1540c-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="1540c-139">Una marca de verificación en esta opción de menú indica que grueso es el ancho actual del lápiz.</span><span class="sxs-lookup"><span data-stu-id="1540c-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Lápiz/fino</span><span class="sxs-lookup"><span data-stu-id="1540c-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="1540c-141">Elige el ancho fino del dibujo.</span><span class="sxs-lookup"><span data-stu-id="1540c-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="1540c-142">Una marca de verificación en esta opción de menú indica que fino es el ancho actual del lápiz.</span><span class="sxs-lookup"><span data-stu-id="1540c-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Receptor/conexión</span><span class="sxs-lookup"><span data-stu-id="1540c-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="1540c-144">Conecta la interfaz IPaperSink de COPaperSink al punto de conexión del objeto de copapeles PaperSink.</span><span class="sxs-lookup"><span data-stu-id="1540c-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="1540c-145">La repintado de la imagen de dibujo actual en [StoClien](structured-storage-client-sample--stoclien-.md) se basa en la conexión del receptor.</span><span class="sxs-lookup"><span data-stu-id="1540c-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="1540c-146">Una marca de verificación en esta opción de menú indica que el repintado está conectado.</span><span class="sxs-lookup"><span data-stu-id="1540c-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Receptor/desconectar</span><span class="sxs-lookup"><span data-stu-id="1540c-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="1540c-148">Desconecta la interfaz IPaperSink de COPaperSink del punto de conexión del objeto de copapeles PaperSink.</span><span class="sxs-lookup"><span data-stu-id="1540c-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="1540c-149">La repintado de la imagen de dibujo actual en [StoClien](structured-storage-client-sample--stoclien-.md) se basa en la conexión del receptor.</span><span class="sxs-lookup"><span data-stu-id="1540c-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="1540c-150">Una marca de verificación en esta opción de menú indica que la repintado está desconectada.</span><span class="sxs-lookup"><span data-stu-id="1540c-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Ayuda/tutorial de StoClien</span><span class="sxs-lookup"><span data-stu-id="1540c-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="1540c-152">Abre el archivo de tutorial de STOCLIEN.HTM en el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="1540c-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Ayuda/tutorial de StoServe</span><span class="sxs-lookup"><span data-stu-id="1540c-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="1540c-154">Abre el archivo de tutorial de STOSERVE.HTM en el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="1540c-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Ayuda/leer archivo de código fuente</span><span class="sxs-lookup"><span data-stu-id="1540c-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="1540c-156">Muestra el cuadro de diálogo abrir para que pueda abrir un archivo de código fuente desde esta lección o desde otro en el Bloc de notas de Windows.</span><span class="sxs-lookup"><span data-stu-id="1540c-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="1540c-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Ayuda/acerca de StoClien</span><span class="sxs-lookup"><span data-stu-id="1540c-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="1540c-158">Muestra el cuadro de diálogo acerca de para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="1540c-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="1540c-159">En el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) se usan muchas de las clases de utilidad y los servicios proporcionados por [APPUTIL](./using-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="1540c-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="1540c-160">Para obtener más información sobre [APPUTIL](./using-visual-studio.md), consulte el código fuente de la biblioteca de [APPUTIL](./using-visual-studio.md) en el directorio de [APPUTIL](./using-visual-studio.md) relacionado y apputil.MD en el directorio principal del tutorial.</span><span class="sxs-lookup"><span data-stu-id="1540c-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="1540c-161">Para obtener más información sobre [APPUTIL](./using-visual-studio.md), consulte [cómo compilar ejemplos](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1540c-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 