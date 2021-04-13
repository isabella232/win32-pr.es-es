---
title: Agregar y modificar eventos
description: Agregar y modificar eventos
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357386"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="b896b-109">Agregar y modificar eventos</span><span class="sxs-lookup"><span data-stu-id="b896b-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="b896b-110">Debe proporcionar controladores de eventos para los eventos de cambio de EN \_ que se producen cuando el usuario cambia el texto en los cuadros de edición de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b896b-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="b896b-111">Estos controladores de eventos tienen una implementación simple que simplemente permite **aplicar** en el cuadro de diálogo Página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b896b-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="b896b-112">Modificar el controlador de eventos de factor de escala</span><span class="sxs-lookup"><span data-stu-id="b896b-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="b896b-113">Debe cambiar el nombre del controlador de eventos existente que el Asistente para complementos proporcionó para el cuadro de edición del factor de escala.</span><span class="sxs-lookup"><span data-stu-id="b896b-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="b896b-114">Debe cambiar el nombre de OnChangeScale a OnChangeDelay en tres ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="b896b-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="b896b-115">En EchoPropPage. h, cambie el nombre en la sección macro de mapa de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b896b-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="b896b-116">Reemplace la línea que asigna el evento de cambio de factor de escala al método OnChangeScale por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="b896b-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="b896b-117">En EchoPropPage. h, cambie el nombre en la línea que cree un prototipo de la función OnChangeScale:</span><span class="sxs-lookup"><span data-stu-id="b896b-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="b896b-118">En EchoPropPage. cpp, cambie el nombre en el encabezado de la función:</span><span class="sxs-lookup"><span data-stu-id="b896b-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="b896b-119">Agregar el controlador de eventos de la combinación húmeda</span><span class="sxs-lookup"><span data-stu-id="b896b-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="b896b-120">Puede agregar fácilmente el controlador de eventos para el \_ evento en cambio que está asociado al control del \_ cuadro de edición IDC WETMIX.</span><span class="sxs-lookup"><span data-stu-id="b896b-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="b896b-121">En el editor de recursos del cuadro de diálogo:</span><span class="sxs-lookup"><span data-stu-id="b896b-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="b896b-122">Haga clic con el botón derecho en el \_ cuadro de edición IDC WETMIX y elija **eventos**.</span><span class="sxs-lookup"><span data-stu-id="b896b-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="b896b-123">Aparecerá el cuadro de diálogo nuevo mensaje de Windows y controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="b896b-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="b896b-124">En el cuadro **clase u objeto que se va a administrar** , haga clic en el nombre del recurso del cuadro de edición, IDC \_ WETMIX.</span><span class="sxs-lookup"><span data-stu-id="b896b-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="b896b-125">En el cuadro **nuevos mensajes o eventos de Windows** , haga clic en \_ cambiar para seleccionarlo.</span><span class="sxs-lookup"><span data-stu-id="b896b-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="b896b-126">Haga clic en **Agregar controlador**.</span><span class="sxs-lookup"><span data-stu-id="b896b-126">Click **Add Handler**.</span></span> <span data-ttu-id="b896b-127">Aparecerá el cuadro de diálogo Agregar función miembro.</span><span class="sxs-lookup"><span data-stu-id="b896b-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="b896b-128">En el cuadro Nombre de la **función miembro** , escriba el nombre OnChangeWetmix.</span><span class="sxs-lookup"><span data-stu-id="b896b-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="b896b-129">Haga clic en **Aceptar** para cerrar el cuadro de diálogo Agregar función miembro.</span><span class="sxs-lookup"><span data-stu-id="b896b-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="b896b-130">Haga clic en **Aceptar** para volver al editor de recursos del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b896b-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="b896b-131">Visual C++ agrega automáticamente el código para el mapa de mensajes y la función de controlador de eventos a EchoPropPage. h.</span><span class="sxs-lookup"><span data-stu-id="b896b-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="b896b-132">El código que inserta proporciona un comentario TODO donde puede Agregar la implementación en el encabezado de la función.</span><span class="sxs-lookup"><span data-stu-id="b896b-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="b896b-133">Se trata de un estilo ligeramente diferente del que usa el código de ejemplo del Asistente para complementos de Windows Media Player, pero es aceptable.</span><span class="sxs-lookup"><span data-stu-id="b896b-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="b896b-134">Si desea escribir la implementación en el archivo de encabezado o moverla a EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="b896b-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="b896b-135">En cualquier caso, la implementación solo necesita una línea de código adicional para habilitar **aplicar** en el cuadro de diálogo de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b896b-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="b896b-136">Inserte esta línea de código antes de la línea que devuelve de la función:</span><span class="sxs-lookup"><span data-stu-id="b896b-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="b896b-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b896b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b896b-138">**Modificar la página de propiedades de ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="b896b-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




