---
description: El objeto PenInputPanel le permite agregar fácilmente entradas manuscritas en contexto a las aplicaciones.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Clase PenInputPanel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697819"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="4162e-103">Clase PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="4162e-103">PenInputPanel class</span></span>

<span data-ttu-id="4162e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4162e-104">\[Deprecated.</span></span> <span data-ttu-id="4162e-105">**PenInputPanel** se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).\]</span><span class="sxs-lookup"><span data-stu-id="4162e-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="4162e-106">El objeto **PenInputPanel** le permite agregar fácilmente entradas manuscritas en contexto a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4162e-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="4162e-107">El objeto **PenInputPanel** está disponible como un objeto que se puede adjuntar y que permite agregar la funcionalidad del panel de entrada de Tablet PC a los controles existentes.</span><span class="sxs-lookup"><span data-stu-id="4162e-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="4162e-108">La interfaz de usuario está asignada en gran medida por el idioma de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="4162e-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="4162e-109">Tiene la opción de elegir el método de entrada predeterminado para el objeto **PenInputPanel** , ya sea escritura a mano o teclado.</span><span class="sxs-lookup"><span data-stu-id="4162e-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="4162e-110">El usuario final puede cambiar entre los métodos de entrada mediante los botones de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4162e-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="4162e-111">**PenInputPanel** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4162e-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="4162e-112">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="4162e-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="4162e-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="4162e-113">Events</span></span>](#events)
-   [<span data-ttu-id="4162e-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4162e-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="4162e-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="4162e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="4162e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4162e-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="4162e-117">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="4162e-117">Enumerations</span></span>

<span data-ttu-id="4162e-118">La clase **PenInputPanel** tiene estas enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="4162e-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="4162e-119">Enumeración</span><span class="sxs-lookup"><span data-stu-id="4162e-119">Enumeration</span></span>                    | <span data-ttu-id="4162e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4162e-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4162e-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="4162e-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="4162e-122">Define el tipo de entrada disponible actualmente en el objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="4162e-123">Events</span><span class="sxs-lookup"><span data-stu-id="4162e-123">Events</span></span>

<span data-ttu-id="4162e-124">La clase **PenInputPanel** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="4162e-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="4162e-125">Evento</span><span class="sxs-lookup"><span data-stu-id="4162e-125">Event</span></span>                                                  | <span data-ttu-id="4162e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="4162e-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4162e-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="4162e-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="4162e-128">Se produce cuando el foco de entrada cambia antes de que el objeto **PenInputPanel** pudiera insertar la entrada del usuario en el control adjunto.</span><span class="sxs-lookup"><span data-stu-id="4162e-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="4162e-129">**PanelChanged**</span><span class="sxs-lookup"><span data-stu-id="4162e-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="4162e-130">Se produce cuando cambia el objeto **PenInputPanel** entre diseños.</span><span class="sxs-lookup"><span data-stu-id="4162e-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="4162e-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="4162e-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="4162e-132">Se produce cuando se mueve el objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="4162e-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="4162e-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="4162e-134">Se produce cuando el objeto **PenInputPanel** se ha mostrado u oculto.</span><span class="sxs-lookup"><span data-stu-id="4162e-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="4162e-135">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4162e-135">Interfaces</span></span>

<span data-ttu-id="4162e-136">La clase **PenInputPanel** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4162e-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="4162e-137">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4162e-137">Interface</span></span>          | <span data-ttu-id="4162e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4162e-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="4162e-139">**IPenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="4162e-139">**IPenInputPanel**</span></span> | <span data-ttu-id="4162e-140">Este objeto implementa la interfaz com **IPenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="4162e-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="4162e-141">Methods</span></span>

<span data-ttu-id="4162e-142">La clase **PenInputPanel** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4162e-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="4162e-143">Método</span><span class="sxs-lookup"><span data-stu-id="4162e-143">Method</span></span>                                                         | <span data-ttu-id="4162e-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="4162e-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4162e-145">**CommitPendingInput**</span><span class="sxs-lookup"><span data-stu-id="4162e-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="4162e-146">Envía la tinta recopilada al reconocedor y envía el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="4162e-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="4162e-147">**EnableTsf**</span><span class="sxs-lookup"><span data-stu-id="4162e-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="4162e-148">Cuando se pasa **true**, el **PenInputPanel** intenta enviar texto al control adjunto a través de Text Services Framework (TSF) y permite el uso de la interfaz de usuario de corrección.</span><span class="sxs-lookup"><span data-stu-id="4162e-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="4162e-149">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="4162e-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="4162e-150">Establece la posición del objeto **PenInputPanel** en una posición de pantalla estática.</span><span class="sxs-lookup"><span data-stu-id="4162e-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="4162e-151">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="4162e-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="4162e-152">Actualiza y restaura las propiedades de **PenInputPanel** en función de la configuración del panel de entrada de Tablet PC, coloca automáticamente el panel de entrada del lápiz y establece la interfaz de usuario en el panel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4162e-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4162e-153">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4162e-153">Properties</span></span>

<span data-ttu-id="4162e-154">La clase **PenInputPanel** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4162e-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="4162e-155">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4162e-155">Property</span></span>                                                                  | <span data-ttu-id="4162e-156">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4162e-156">Access type</span></span>           | <span data-ttu-id="4162e-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="4162e-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4162e-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="4162e-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="4162e-159">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-159">Read/write</span></span><br/> | <span data-ttu-id="4162e-160">Obtiene o establece el identificador de ventana del control al que está asociado el objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="4162e-161">**Automostrar**</span><span class="sxs-lookup"><span data-stu-id="4162e-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="4162e-162">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-162">Read/write</span></span><br/> | <span data-ttu-id="4162e-163">Obtiene o establece un valor booleano que especifica si el objeto **PenInputPanel** aparece cuando el foco se establece usando el lápiz.</span><span class="sxs-lookup"><span data-stu-id="4162e-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="4162e-164">**Disponibles**</span><span class="sxs-lookup"><span data-stu-id="4162e-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="4162e-165">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4162e-165">Read-only</span></span><br/>  | <span data-ttu-id="4162e-166">Obtiene un valor booleano que especifica si el objeto **PenInputPanel** está procesando actualmente la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4162e-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="4162e-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="4162e-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="4162e-168">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-168">Read/write</span></span><br/> | <span data-ttu-id="4162e-169">Obtiene o establece el tipo de panel que se está usando actualmente para la entrada dentro del objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="4162e-170">**DefaultPanel**</span><span class="sxs-lookup"><span data-stu-id="4162e-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="4162e-171">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-171">Read/write</span></span><br/> | <span data-ttu-id="4162e-172">Obtiene o establece el tipo de panel predeterminado que se usa para la entrada dentro del objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="4162e-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="4162e-173">**Factoid**</span><span class="sxs-lookup"><span data-stu-id="4162e-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="4162e-174">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-174">Read/write</span></span><br/> | <span data-ttu-id="4162e-175">Obtiene o establece el nombre de cadena del Factoid que se usa en el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="4162e-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="4162e-176">**Height**</span><span class="sxs-lookup"><span data-stu-id="4162e-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="4162e-177">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4162e-177">Read-only</span></span><br/>  | <span data-ttu-id="4162e-178">Obtiene el alto del objeto **PenInputPanel** en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="4162e-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4162e-179">**HorizontalOffset**</span><span class="sxs-lookup"><span data-stu-id="4162e-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="4162e-180">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-180">Read/write</span></span><br/> | <span data-ttu-id="4162e-181">Obtiene o establece el desplazamiento entre el borde izquierdo del objeto **PenInputPanel** y el borde izquierdo del control al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="4162e-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="4162e-182">**Salido**</span><span class="sxs-lookup"><span data-stu-id="4162e-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="4162e-183">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4162e-183">Read-only</span></span><br/>  | <span data-ttu-id="4162e-184">Obtiene la ubicación horizontal, o eje x, del borde izquierdo del objeto **PenInputPanel** , en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4162e-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="4162e-185">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="4162e-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="4162e-186">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4162e-186">Read-only</span></span><br/>  | <span data-ttu-id="4162e-187">Obtiene la ubicación vertical, o eje y, del borde superior del objeto **PenInputPanel** , en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4162e-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="4162e-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="4162e-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="4162e-189">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-189">Read/write</span></span><br/> | <span data-ttu-id="4162e-190">Obtiene o establece el desplazamiento entre el borde horizontal más cercano del objeto **PenInputPanel** y el borde horizontal más cercano del control al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="4162e-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="4162e-191">**Visible**</span><span class="sxs-lookup"><span data-stu-id="4162e-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="4162e-192">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4162e-192">Read/write</span></span><br/> | <span data-ttu-id="4162e-193">Obtiene o establece un valor que indica si el objeto **PenInputPanel** está visible.</span><span class="sxs-lookup"><span data-stu-id="4162e-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="4162e-194">**Width**</span><span class="sxs-lookup"><span data-stu-id="4162e-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="4162e-195">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4162e-195">Read-only</span></span><br/>  | <span data-ttu-id="4162e-196">Obtiene el ancho del objeto **PenInputPanel** en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="4162e-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="4162e-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4162e-197">Remarks</span></span>

<span data-ttu-id="4162e-198">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="4162e-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="4162e-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4162e-199">Requirements</span></span>



| <span data-ttu-id="4162e-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="4162e-200">Requirement</span></span> | <span data-ttu-id="4162e-201">Value</span><span class="sxs-lookup"><span data-stu-id="4162e-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4162e-202">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4162e-202">Minimum supported client</span></span><br/> | <span data-ttu-id="4162e-203">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4162e-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4162e-204">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4162e-204">Minimum supported server</span></span><br/> | <span data-ttu-id="4162e-205">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4162e-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4162e-206">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4162e-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="4162e-207"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4162e-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4162e-208">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4162e-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="4162e-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4162e-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4162e-210">Vea también</span><span class="sxs-lookup"><span data-stu-id="4162e-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4162e-211">Programar el panel de entrada mediante la clase PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="4162e-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
