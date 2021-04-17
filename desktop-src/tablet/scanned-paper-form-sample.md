---
description: En este ejemplo de C, se ha \# analizado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un control InkPicture. En el ejemplo se usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Ejemplo de formulario de papel digitalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716449"
---
# <a name="scanned-paper-form-sample"></a>Ejemplo de formulario de papel digitalizado

En este ejemplo de C, se ha \# analizado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un control [InkPicture](/previous-versions/aa514604(v=msdn.10)) . En el ejemplo se usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.

El ejemplo incluye un archivo lenguaje de marcado extensible (XML) Formdata.xml. El archivo XML contiene el nombre del archivo PNG. También contiene `FieldInfo` elementos que definen regiones rectangulares en el formulario donde un usuario puede escribir entradas manuscritas. La información en el `FieldInfo` elemento se muestra en el ejemplo siguiente:


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Los elementos izquierdo, superior, derecho e inferior son definiciones de coordenadas de píxeles para cada campo.

El ejemplo Inicializa un nuevo [conjunto](/dotnet/api/system.data.dataset?view=netcore-3.1) de datos con los datos contenidos en Formdata.xml:


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



La imagen de formulario especificada en Formdata.xml se carga como el fondo del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



A continuación, se habilita la recopilación de tinta para el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Controladores de eventos de menú

La aplicación incluye controladores de eventos de clic para todos los menús mostrados en la parte superior del formulario.

### <a name="recognize-menu-item"></a>Elemento de menú Recognize

El controlador de eventos de clic en el menú reconocer deshabilita la recopilación de entradas manuscritas del control y comprueba si hay un reconocedor de escritura a mano. Si no hay ningún reconocedor instalado, se muestra un cuadro de diálogo. Un usuario debe hacer clic en la opción de menú tinta o lápiz para volver a habilitar el control para la entrada de lápiz.

Si se instala un reconocedor, la `Recognize` función recupera los datos XML que especifican las coordenadas de píxel para cada campo de formulario. Las coordenadas se convierten en coordenadas de espacio de la tinta y se define un rectángulo para cada campo de formulario. Una vez definidos los rectángulos, la función busca los trazos que se cruzan y se encuentran dentro de cada rectángulo. Por último, realiza el reconocimiento de la tinta y muestra los resultados en un cuadro de mensaje.

### <a name="ink-menu-item"></a>Elemento de menú de entrada manuscrita

El controlador de eventos de clic de menú de tinta habilita el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) .

### <a name="pen-menu-item"></a>Elemento de menú de lápiz

El controlador de eventos Click del menú lápiz realiza las siguientes tareas:

-   Deshabilita la recopilación de entradas manuscritas del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) (que es necesario antes de cambiar la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) ).
-   Establece la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) para recopilar la entrada de lápiz.
-   Vuelve a habilitar la recopilación de entradas manuscritas del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) y activa o desactiva los menús de lápiz, seleccionar y borrador para indicar el modo activo.

### <a name="edit-menu-item"></a>Editar elemento de menú

El controlador de eventos Click del menú edición es similar al controlador de eventos del menú pluma. Realiza las tareas siguientes:

-   Deshabilita la recopilación de entradas manuscritas.
-   Establece la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) en **Select**, que permite al usuario realizar la selección de entradas manuscritas.
-   Vuelve a habilitar la recopilación de entradas manuscritas y alterna los menús de pluma, edición y borrador para indicar el modo activo.

### <a name="eraser-menu-item"></a>Elemento de menú de borrador

El controlador de eventos de clic de menú de borrador establece el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) en **Delete**, lo que permite al usuario borrar la tinta. También alterna los elementos de menú de lápiz, edición y borrador.

### <a name="clear-menu-item"></a>Borrar elemento de menú

El controlador de eventos de clic de menú borrar elimina la colección de [trazos](/previous-versions/ms552701(v=vs.100)) actual del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) , con lo que se borran todas las entradas de lápiz del formulario.

## <a name="closing-the-form"></a>Cierre del formulario

En el código generado por el diseñador de Windows Forms, el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agrega a la lista de componentes del formulario cuando se inicializa el formulario. Cuando se cierra el formulario, se desecha el control InkPicture, así como los demás componentes del formulario, mediante el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control InkEdit](inkedit-control.md)
</dt> <dt>

[InkPicture (control)](inkpicture-control.md)
</dt> </dl>

 

 
