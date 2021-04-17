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
# <a name="peninputpanel-sample"></a>Ejemplo de PenInputPanel

Este ejemplo se basa en el ejemplo de formulario de notificaciones automáticas mediante la integración del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . El ejemplo se encuentra en el \# directorio C PIPanel de la carpeta Autoclaims.

> [!Note]  
> Este ejemplo requiere que el sistema esté equipado con un dispositivo de lápiz. Si usa simplemente un mouse (u otro dispositivo señalador de dispositivo de interfaz no humana (HID)), el [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) no aparece.

 

Para obtener más información sobre el ejemplo de formulario de notificaciones automáticas, consulte [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md). Para obtener más información sobre el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consulte [programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).

En el ejemplo, el formulario notificaciones automáticas contiene cinco campos a los que se pide al usuario que ponga información relevante sobre la reclamación: el número de la Directiva, el nombre asegurado, el año, la marca y el modelo del automóvil. Un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) se adjunta a cada campo de entrada para proporcionar un medio sencillo para escribir valores con un lápiz.

Hay dos técnicas para adjuntar un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a los campos de entrada del formulario. La primera técnica consiste en asignar una instancia independiente del objeto a cada campo de entrada en tiempo de diseño. La segunda consiste en crear una instancia única del objeto y, a continuación, adjuntar esa instancia de objeto en tiempo de ejecución a un campo cuando recibe el foco. En este ejemplo se muestran ambas técnicas.

Existen contrapartidas para decidir qué técnica usar. La creación de una instancia única del objeto para cada campo de formulario requiere un poco más de memoria cuando se carga el formulario. Sin embargo, evita tener que controlar los eventos de foco de los campos para asignar una sola instancia al campo actual en tiempo de ejecución.

Dado que el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) solo se admite en un Tablet PC, el ejemplo crea los objetos PenInputPanel dentro de un bloque de control de excepciones.

## <a name="one-object-per-field"></a>Un objeto por campo

En el ejemplo se muestra la primera técnica (un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) asignando los campos de entrada para el número de directiva ( `inkEdPolicyNumber` ) y el nombre asegurado ( `inkEdName` ) a una instancia única del objeto PenInputPanel. Un constructor sobrecargado para el objeto PenInputPanel puede tomar el nombre del control de entrada como argumento, con lo que se asocian los controles. En las líneas siguientes del controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario se muestra lo siguiente:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Un objeto por formulario

La segunda técnica también se muestra en el ejemplo: una única instancia de un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , se comparte entre los campos de entrada Year, make y Model. El objeto compartido se crea mediante el constructor predeterminado.


```C++
pipShared = new PenInputPanel();
```



El uso de esta técnica requiere que el formulario tenga solo una instancia del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Esto ahorra memoria, pero debe agregar código para controlar el evento cuando un campo de entrada recibe el foco. Cuando un control que usa una instancia compartida de un objeto PenInputPanel obtiene el foco, establezca la propiedad [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) del objeto PenInputPanel en ese control. En el código siguiente se muestra un controlador de eventos para los eventos de los campos Year, make y Model `Enter` .


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



Asegúrese de establecer las propiedades que se deben establecer al cambiar el foco a un nuevo control. En los controladores de eventos anteriores, por ejemplo, la propiedad [Factoid](/previous-versions/ms571978(v=vs.100)) se establece según corresponda.

## <a name="usability-considerations"></a>Consideraciones de facilidad de uso

Tenga en cuenta las siguientes consideraciones de facilidad de uso al usar el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) en la aplicación.

### <a name="positioning-the-peninputpanel"></a>Colocar el PenInputPanel

Dado que los campos se colocan verticalmente en el formulario en este ejemplo, la interfaz de usuario de [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada control de entrada se coloca ligeramente a la derecha del control de entrada para que sea más fácil de usar. Esto evita que el PenInputPanel abarque el siguiente cuadro de edición, lo que facilita el destino del siguiente cuadro de edición.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Seleccionar el panel de entrada para mostrar

Dado que los números de directiva suelen ser combinaciones de números, letras y otros caracteres, pueden ser propensos a la detección de errores. Por lo tanto, el ejemplo establece el panel predeterminado que muestra el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como el teclado cuando se adjunta al campo de número de la Directiva.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



El comportamiento predeterminado del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) es usar el panel que el usuario seleccionó en último lugar.

### <a name="text-services-framework-correction-user-interface"></a>Interfaz de usuario de corrección del marco de trabajo de servicios de texto

En este ejemplo, todos los campos de entrada son controles [InkEdit](/previous-versions/ms552265(v=vs.100)) . Esto es importante porque el control InkEdit tiene compatibilidad integrada con el marco de [trabajo de servicios de texto](../tsf/text-services-framework.md) (TSF) y, por tanto, es capaz de admitir la interfaz de usuario de corrección en contexto para la entrada recibida del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .

El valor predeterminado de [EnableTsf](/previous-versions/ms569656(v=vs.100)) es **true**. Esto hace que el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) intente iniciar el marco de trabajo de servicios de texto (TSF) en el control adjunto. Si es correcto, la interfaz de usuario de corrección se muestra en el control y permite el acceso a alternativas de reconocimiento. La llamada a este método con un parámetro **false** intenta apagar TSF en el control adjunto.

El control [InkEdit](/previous-versions/ms552265(v=vs.100)) ya proporciona una interfaz de usuario de corrección, pero en el ejemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) se usa para permitir que [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) use el contexto del REconocedor de inserción de TSF en lugar de la función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar los resultados del reconocimiento de escritura a mano en el control. El resultado es que se puede insertar texto incluso si el campo ya no tiene el foco.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Cierre del formulario

En el código generado por el diseñador de Windows Forms, los controles [InkEdit](/previous-versions/ms552265(v=vs.100)) y [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agregan a la lista de componentes del formulario cuando se inicializa el formulario. Cuando se cierra el formulario, los controles InkEdit y InkPicture se eliminan, así como los demás componentes del formulario, mediante el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario. El método Dispose del formulario también desecha los objetos de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) creados para el formulario.

 

 
