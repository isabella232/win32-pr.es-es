---
description: Este ejemplo se basa en el ejemplo de formulario de notificaciones automáticas mediante la integración del objeto PenInputPanel. El ejemplo se encuentra en el \# directorio C PIPanel de la carpeta Autoclaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Ejemplo de PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697662"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="3ce48-104">Ejemplo de PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="3ce48-104">PenInputPanel Sample</span></span>

<span data-ttu-id="3ce48-105">Este ejemplo se basa en el ejemplo de formulario de notificaciones automáticas mediante la integración del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3ce48-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="3ce48-106">El ejemplo se encuentra en el \# directorio C PIPanel de la carpeta Autoclaims.</span><span class="sxs-lookup"><span data-stu-id="3ce48-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="3ce48-107">Este ejemplo requiere que el sistema esté equipado con un dispositivo de lápiz.</span><span class="sxs-lookup"><span data-stu-id="3ce48-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="3ce48-108">Si usa simplemente un mouse (u otro dispositivo señalador de dispositivo de interfaz no humana (HID)), el [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) no aparece.</span><span class="sxs-lookup"><span data-stu-id="3ce48-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="3ce48-109">Para obtener más información sobre el ejemplo de formulario de notificaciones automáticas, consulte [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3ce48-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="3ce48-110">Para obtener más información sobre el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consulte [programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).</span><span class="sxs-lookup"><span data-stu-id="3ce48-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="3ce48-111">En el ejemplo, el formulario notificaciones automáticas contiene cinco campos a los que se pide al usuario que ponga información relevante sobre la reclamación: el número de la Directiva, el nombre asegurado, el año, la marca y el modelo del automóvil.</span><span class="sxs-lookup"><span data-stu-id="3ce48-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="3ce48-112">Un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) se adjunta a cada campo de entrada para proporcionar un medio sencillo para escribir valores con un lápiz.</span><span class="sxs-lookup"><span data-stu-id="3ce48-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="3ce48-113">Hay dos técnicas para adjuntar un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a los campos de entrada del formulario.</span><span class="sxs-lookup"><span data-stu-id="3ce48-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="3ce48-114">La primera técnica consiste en asignar una instancia independiente del objeto a cada campo de entrada en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="3ce48-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="3ce48-115">La segunda consiste en crear una instancia única del objeto y, a continuación, adjuntar esa instancia de objeto en tiempo de ejecución a un campo cuando recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="3ce48-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="3ce48-116">En este ejemplo se muestran ambas técnicas.</span><span class="sxs-lookup"><span data-stu-id="3ce48-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="3ce48-117">Existen contrapartidas para decidir qué técnica usar.</span><span class="sxs-lookup"><span data-stu-id="3ce48-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="3ce48-118">La creación de una instancia única del objeto para cada campo de formulario requiere un poco más de memoria cuando se carga el formulario.</span><span class="sxs-lookup"><span data-stu-id="3ce48-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="3ce48-119">Sin embargo, evita tener que controlar los eventos de foco de los campos para asignar una sola instancia al campo actual en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3ce48-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="3ce48-120">Dado que el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) solo se admite en un Tablet PC, el ejemplo crea los objetos PenInputPanel dentro de un bloque de control de excepciones.</span><span class="sxs-lookup"><span data-stu-id="3ce48-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="3ce48-121">Un objeto por campo</span><span class="sxs-lookup"><span data-stu-id="3ce48-121">One Object per Field</span></span>

<span data-ttu-id="3ce48-122">En el ejemplo se muestra la primera técnica (un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) asignando los campos de entrada para el número de directiva ( `inkEdPolicyNumber` ) y el nombre asegurado ( `inkEdName` ) a una instancia única del objeto PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="3ce48-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="3ce48-123">Un constructor sobrecargado para el objeto PenInputPanel puede tomar el nombre del control de entrada como argumento, con lo que se asocian los controles.</span><span class="sxs-lookup"><span data-stu-id="3ce48-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="3ce48-124">En las líneas siguientes del controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario se muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3ce48-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="3ce48-125">Un objeto por formulario</span><span class="sxs-lookup"><span data-stu-id="3ce48-125">One Object per Form</span></span>

<span data-ttu-id="3ce48-126">La segunda técnica también se muestra en el ejemplo: una única instancia de un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , se comparte entre los campos de entrada Year, make y Model.</span><span class="sxs-lookup"><span data-stu-id="3ce48-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="3ce48-127">El objeto compartido se crea mediante el constructor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3ce48-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="3ce48-128">El uso de esta técnica requiere que el formulario tenga solo una instancia del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3ce48-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="3ce48-129">Esto ahorra memoria, pero debe agregar código para controlar el evento cuando un campo de entrada recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="3ce48-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="3ce48-130">Cuando un control que usa una instancia compartida de un objeto PenInputPanel obtiene el foco, establezca la propiedad [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) del objeto PenInputPanel en ese control.</span><span class="sxs-lookup"><span data-stu-id="3ce48-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="3ce48-131">En el código siguiente se muestra un controlador de eventos para los eventos de los campos Year, make y Model `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3ce48-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="3ce48-132">Asegúrese de establecer las propiedades que se deben establecer al cambiar el foco a un nuevo control.</span><span class="sxs-lookup"><span data-stu-id="3ce48-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="3ce48-133">En los controladores de eventos anteriores, por ejemplo, la propiedad [Factoid](/previous-versions/ms571978(v=vs.100)) se establece según corresponda.</span><span class="sxs-lookup"><span data-stu-id="3ce48-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="3ce48-134">Consideraciones de facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="3ce48-134">Usability Considerations</span></span>

<span data-ttu-id="3ce48-135">Tenga en cuenta las siguientes consideraciones de facilidad de uso al usar el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ce48-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="3ce48-136">Colocar el PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="3ce48-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="3ce48-137">Dado que los campos se colocan verticalmente en el formulario en este ejemplo, la interfaz de usuario de [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada control de entrada se coloca ligeramente a la derecha del control de entrada para que sea más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="3ce48-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="3ce48-138">Esto evita que el PenInputPanel abarque el siguiente cuadro de edición, lo que facilita el destino del siguiente cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="3ce48-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="3ce48-139">Seleccionar el panel de entrada para mostrar</span><span class="sxs-lookup"><span data-stu-id="3ce48-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="3ce48-140">Dado que los números de directiva suelen ser combinaciones de números, letras y otros caracteres, pueden ser propensos a la detección de errores.</span><span class="sxs-lookup"><span data-stu-id="3ce48-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="3ce48-141">Por lo tanto, el ejemplo establece el panel predeterminado que muestra el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como el teclado cuando se adjunta al campo de número de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="3ce48-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="3ce48-142">El comportamiento predeterminado del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) es usar el panel que el usuario seleccionó en último lugar.</span><span class="sxs-lookup"><span data-stu-id="3ce48-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="3ce48-143">Interfaz de usuario de corrección del marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="3ce48-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="3ce48-144">En este ejemplo, todos los campos de entrada son controles [InkEdit](/previous-versions/ms552265(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="3ce48-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="3ce48-145">Esto es importante porque el control InkEdit tiene compatibilidad integrada con el marco de [trabajo de servicios de texto](../tsf/text-services-framework.md) (TSF) y, por tanto, es capaz de admitir la interfaz de usuario de corrección en contexto para la entrada recibida del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3ce48-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="3ce48-146">El valor predeterminado de [EnableTsf](/previous-versions/ms569656(v=vs.100)) es **true**.</span><span class="sxs-lookup"><span data-stu-id="3ce48-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="3ce48-147">Esto hace que el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) intente iniciar el marco de trabajo de servicios de texto (TSF) en el control adjunto.</span><span class="sxs-lookup"><span data-stu-id="3ce48-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="3ce48-148">Si es correcto, la interfaz de usuario de corrección se muestra en el control y permite el acceso a alternativas de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="3ce48-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="3ce48-149">La llamada a este método con un parámetro **false** intenta apagar TSF en el control adjunto.</span><span class="sxs-lookup"><span data-stu-id="3ce48-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="3ce48-150">El control [InkEdit](/previous-versions/ms552265(v=vs.100)) ya proporciona una interfaz de usuario de corrección, pero en el ejemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) se usa para permitir que [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) use el contexto del REconocedor de inserción de TSF en lugar de la función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar los resultados del reconocimiento de escritura a mano en el control.</span><span class="sxs-lookup"><span data-stu-id="3ce48-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="3ce48-151">El resultado es que se puede insertar texto incluso si el campo ya no tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="3ce48-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="3ce48-152">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="3ce48-152">Closing the Form</span></span>

<span data-ttu-id="3ce48-153">En el código generado por el diseñador de Windows Forms, los controles [InkEdit](/previous-versions/ms552265(v=vs.100)) y [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agregan a la lista de componentes del formulario cuando se inicializa el formulario.</span><span class="sxs-lookup"><span data-stu-id="3ce48-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="3ce48-154">Cuando se cierra el formulario, los controles InkEdit y InkPicture se eliminan, así como los demás componentes del formulario, mediante el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="3ce48-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="3ce48-155">El método Dispose del formulario también desecha los objetos de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) creados para el formulario.</span><span class="sxs-lookup"><span data-stu-id="3ce48-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
