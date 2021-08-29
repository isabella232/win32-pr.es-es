---
description: En este ejemplo de C, se ha examinado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un \# control InkPicture. El ejemplo usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Ejemplo de formulario de papel digitalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8493384cecdfdbf0186692d52642307f720502f4b953724f444df400cc83c96a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934705"
---
# <a name="scanned-paper-form-sample"></a>Ejemplo de formulario de papel digitalizado

En este ejemplo de C, se ha examinado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un \# control [InkPicture.](/previous-versions/aa514604(v=msdn.10)) El ejemplo usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.

El ejemplo incluye un archivo lenguaje de marcado extensible (XML), Formdata.xml. El archivo XML contiene el nombre del archivo PNG. También contiene elementos `FieldInfo` que definen regiones rectangulares en el formulario donde un usuario puede escribir entrada de lápiz. La información del `FieldInfo` elemento se muestra en el ejemplo siguiente:


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Los elementos Left, Top, Right e Bottom son definiciones de coordenadas de píxel para cada campo.

El ejemplo inicializa un nuevo [conjunto de datos](/dotnet/api/system.data.dataset?view=netcore-3.1) con los datos incluidos en Formdata.xml:


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



La imagen de formulario especificada en Formdata.xml se carga como fondo del control [InkPicture:](/previous-versions/aa514604(v=msdn.10))


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



A continuación, la colección ink se habilita para el control [InkPicture:](/previous-versions/aa514604(v=msdn.10))


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Controladores de eventos de menú

La aplicación incluye controladores de eventos click para todos los menús que se muestran en la parte superior del formulario.

### <a name="recognize-menu-item"></a>Reconocer elemento de menú

El controlador de eventos de clic del menú Reconocer deshabilita la recopilación de lápiz para el control y comprueba si hay un reconocedor de escritura a mano. Si no hay ningún reconocedor instalado, se muestra un cuadro de diálogo. A continuación, un usuario debe hacer clic en la opción de menú Ink o Pen para volver a habilitar el control para la entrada de lápiz.

Si se instala un reconocedor, la función recupera los datos XML que especifican coordenadas `Recognize` de píxel para cada campo de formulario. Las coordenadas se convierten en coordenadas de espacio de entrada de lápiz y se define un rectángulo para cada campo de formulario. Una vez definidos los rectángulos, la función busca los trazos que se intersecan y se encuentran dentro de cada rectángulo. Por último, realiza el reconocimiento en la entrada de lápiz y muestra los resultados en un cuadro de mensaje.

### <a name="ink-menu-item"></a>Elemento de menú Ink

El controlador de eventos de clic del menú Ink habilita el control [InkPicture.](/previous-versions/aa514604(v=msdn.10))

### <a name="pen-menu-item"></a>Elemento de menú Del lápiz

El controlador de eventos de clic del menú Lápiz realiza las siguientes tareas:

-   Deshabilita la colección de lápiz para el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) (que es necesario antes de cambiar la [propiedad EditingMode).](/previous-versions/ms582189(v=vs.100))
-   Establece la [propiedad EditingMode](/previous-versions/ms582189(v=vs.100)) para recopilar la entrada de lápiz.
-   Vuelve a habilitar la recopilación de lápiz para el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) y alterna los menús Lápiz, Seleccionar y Borrador para indicar el modo activo.

### <a name="edit-menu-item"></a>Editar elemento de menú

El controlador de eventos De clic del menú Editar es similar al controlador de eventos del menú Lápiz. Realiza las siguientes tareas:

-   Deshabilita la colección de entrada de lápiz.
-   Establece la [propiedad EditingMode](/previous-versions/ms582189(v=vs.100)) en **Select**, que permite al usuario realizar la selección de entrada de lápiz.
-   Vuelve a habilitar la recopilación de lápiz y alterna los menús Lápiz, Edición y Borrador para indicar el modo activo.

### <a name="eraser-menu-item"></a>Elemento de menú Borrador

El controlador de eventos de clic del menú Borrador establece el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) en **Delete**, lo que permite a un usuario borrar la entrada de lápiz. También alterna los elementos de menú Lápiz, Edición y Borrador.

### <a name="clear-menu-item"></a>Borrar elemento de menú

El controlador de eventos de clic del menú Borrar elimina la colección [Strokes](/previous-versions/ms552701(v=vs.100)) actual para el control [InkPicture,](/previous-versions/aa514604(v=msdn.10)) borrando así toda la entrada de lápiz del formulario.

## <a name="closing-the-form"></a>Cerrar el formulario

En el Windows generado por el Diseñador de formularios, el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agrega a la lista de componentes del formulario cuando se inicializa el formulario. Cuando se cierra el formulario, el método Dispose del formulario elimina el control InkPicture, así como los demás componentes [del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) formulario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[InkEdit Control](inkedit-control.md)
</dt> <dt>

[InkPicture Control](inkpicture-control.md)
</dt> </dl>

 

 
