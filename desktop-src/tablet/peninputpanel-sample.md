---
description: Este ejemplo se basa en el ejemplo de formulario de notificaciones automáticas mediante la integración del objeto PenInputPanel. El ejemplo se encuentra en el directorio PIPanel de C \# de la carpeta AutoClaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Ejemplo de PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934745"
---
# <a name="peninputpanel-sample"></a>Ejemplo de PenInputPanel

Este ejemplo se basa en el ejemplo de formulario de notificaciones automáticas mediante la integración del [objeto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) El ejemplo se encuentra en el directorio PIPanel de C \# de la carpeta AutoClaims.

> [!Note]  
> Este ejemplo requiere que el sistema esté equipado con un dispositivo de lápiz. Si solo usa un mouse (u otro dispositivo que apunta a un dispositivo de interfaz no humana (HID), [penInputPanel](/previous-versions/aa514041(v=msdn.10)) no aparece.

 

Para obtener más información sobre el ejemplo de formulario de notificaciones automáticas, vea [Ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md). Para obtener más información sobre [el objeto PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) vea [Programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).

En el ejemplo, el formulario de notificaciones automáticas contiene cinco campos en los que se pide al usuario que coloque información relevante para la notificación: número de directiva, nombre de la licencia, año, marca y modelo del automóvil. Un [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) se adjunta a cada campo de entrada para proporcionar un medio sencillo para escribir valores con un lápiz.

Hay dos técnicas para adjuntar un [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a los campos de entrada del formulario. La primera técnica consiste en asignar una instancia independiente del objeto a cada campo de entrada en tiempo de diseño. La segunda es crear una instancia única del objeto y, a continuación, adjuntar esa instancia de objeto en tiempo de ejecución a un campo cuando recibe el foco. En este ejemplo se muestran ambas técnicas.

Hay algunos contras implicados en la decisión de la técnica que se va a usar. La creación de una instancia única del objeto para cada campo de formulario requiere algo más de memoria cuando se carga el formulario. Sin embargo, ahorra tener que controlar los eventos de foco para que los campos asignen una única instancia al campo actual en tiempo de ejecución.

Dado que [el objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) solo se admite en un tablet PC, el ejemplo crea los objetos PenInputPanel dentro de un bloque de control de excepciones.

## <a name="one-object-per-field"></a>Un objeto por campo

En el ejemplo se muestra la primera técnica (un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) mediante la asignación de los campos de entrada para el número de directiva ( ) y el nombre de la propiedad ( ) una instancia única del `inkEdPolicyNumber` `inkEdName` objeto PenInputPanel. Un constructor sobrecargado para el objeto PenInputPanel puede tomar el nombre del control de entrada como argumento, asociando así los controles. Las líneas siguientes del controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario lo muestran:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Un objeto por formulario

La segunda técnica también se muestra en el ejemplo: una única instancia de un objeto [PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) , se comparte entre los campos de entrada Year, Make y `pipShared` Model. El objeto compartido se crea mediante el constructor predeterminado.


```C++
pipShared = new PenInputPanel();
```



El uso de esta técnica requiere que el formulario tenga solo una única instancia del [objeto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Esto ahorra memoria, pero debe agregar código para controlar el evento cuando un campo de entrada recibe el foco. Cuando un control que usa una instancia compartida de un objeto PenInputPanel obtiene el foco, establezca la propiedad [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) del objeto PenInputPanel en ese control. El código siguiente muestra un controlador de eventos para los eventos de los campos Year, Make y `Enter` Model.


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



Asegúrese de establecer las propiedades que deben establecerse cuando el foco cambie a un nuevo control. En los controladores de eventos anteriores, por ejemplo, la [propiedad Factoid](/previous-versions/ms571978(v=vs.100)) se establece según corresponda.

## <a name="usability-considerations"></a>Consideraciones de facilidad de uso

Tenga en cuenta las siguientes consideraciones de facilidad de uso al usar el [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) en la aplicación.

### <a name="positioning-the-peninputpanel"></a>Colocación de PenInputPanel

Dado que los campos están dispuestos verticalmente en el formulario de este ejemplo, la interfaz de usuario [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada control de entrada se coloca ligeramente a la derecha del control de entrada para facilitar su uso. Esto evita que PenInputPanel encubre el siguiente cuadro de edición, lo que facilita el destino del siguiente cuadro de edición.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Selección del Panel de entrada para mostrar

Dado que los números de directiva suelen ser combinaciones de números, letras y otros caracteres, pueden ser propensos a errores de reconocimiento. Por lo tanto, el ejemplo establece el panel predeterminado que muestra el [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para que sea el teclado cuando se adjunta al campo de número de directiva.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



El comportamiento predeterminado del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) es usar el panel que el usuario seleccionó en último lugar.

### <a name="text-services-framework-correction-user-interface"></a>Text Services Framework corrección Interfaz de usuario

En este ejemplo, todos los campos de entrada son [controles InkEdit.](/previous-versions/ms552265(v=vs.100)) Esto es significativo porque el control InkEdit tiene compatibilidad integrada con [Text Services Framework](../tsf/text-services-framework.md) (TSF) y, por tanto, es capaz de admitir la interfaz de usuario de corrección local para la entrada recibida del objeto [PenInputPanel.](/previous-versions/aa514041(v=msdn.10))

El valor predeterminado de [EnableTsf](/previous-versions/ms569656(v=vs.100)) es **TRUE.** Esto hace que [el objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) intente iniciar el Text Services Framework (TSF) en el control asociado. Si se realiza correctamente, la interfaz de usuario de corrección se muestra en el control y permite el acceso a alternativas de reconocimiento. Llamar a este método con **un parámetro FALSE** intenta apagar TSF en el control adjunto.

El control [InkEdit](/previous-versions/ms552265(v=vs.100)) ya proporciona una interfaz de usuario de corrección, pero en el ejemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) se usa para permitir que [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) use el contexto del reconocedor de inserción de TSF en lugar de la [**función SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar los resultados del reconocimiento de escritura a mano al control. El resultado es que el texto se puede insertar incluso si el campo ya no tiene el foco.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Cerrar el formulario

En el Windows generado por el Diseñador de formularios, los controles [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agregan a la lista de componentes del formulario cuando se inicializa el formulario. Cuando se cierra el formulario, el método Dispose del formulario elimina los controles InkEdit e InkPicture, así como los demás componentes [del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) formulario. El método Dispose del formulario también elimina los objetos [Ink](/previous-versions/aa515768(v=msdn.10)) que se crean para el formulario.

 

 
