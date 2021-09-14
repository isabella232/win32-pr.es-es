---
title: Asegurarse de que los elementos de la interfaz de usuario tienen el nombre correcto
description: En este tema se describe la manera correcta de especificar los nombres de los elementos de la interfaz de usuario en las aplicaciones win32 de Microsoft para que Microsoft Active Accessibility pueda exponer con precisión los nombres a las aplicaciones cliente a través de IAccessible \ 32; Propiedad Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168577"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Asegurarse de que los elementos de la interfaz de usuario tienen el nombre correcto

En este tema se describe la manera correcta de especificar los nombres de los elementos de la interfaz de usuario en las aplicaciones win32 de Microsoft para que Microsoft Active Accessibility pueda exponer con precisión los nombres a las aplicaciones cliente a través de la propiedad [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md).

La información de esta sección solo se aplica Microsoft Active Accessibility datos. No se aplica a las aplicaciones que usan Microsoft Automatización de la interfaz de usuario o a las basadas en lenguajes de marcado como HTML, HTML dinámico (DHTML) o XML.

-   [Información general](#overview)
-   [Cómo causa problemas la nomenclatura incorrecta](#how-incorrect-naming-causes-problems)
-   [Cómo obtiene MSAA la propiedad Name](#how-msaa-gets-the-name-property)
-   [Cómo buscar y corregir problemas de nomenclatura](#how-to-find-and-correct-naming-problems)
-   [Cómo nombrar correctamente una barra de seguimiento](#how-to-correctly-name-a-trackbar)
-   [Cómo usar etiquetas invisibles para dar nombre a controles](#how-to-use-invisible-labels-to-name-controls)
-   [Cómo usar la anotación directa para especificar la propiedad Name](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Pasos para anotar la propiedad Name](#steps-for-annotating-the-name-property)
    -   [Ejemplo de anotación de la propiedad Name](#example-of-annotating-the-name-property)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

En Microsoft Active Accessibility, cada elemento de la interfaz de usuario de una aplicación se representa mediante un objeto que expone la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Las aplicaciones cliente usan las propiedades y los métodos de la **interfaz IAccessible** para interactuar con el elemento de la interfaz de usuario y recuperar información sobre él. Una de las propiedades más importantes expuestas por la **interfaz IAccessible** es la [propiedad Name](name-property.md). Las aplicaciones cliente se basan en la propiedad Name para buscar, identificar o anunciar un elemento de interfaz de usuario al usuario. Si Microsoft Active Accessibility puede exponer correctamente la propiedad Name de un elemento de interfaz de usuario determinado, las aplicaciones cliente no podrán presentar ese elemento de interfaz de usuario al usuario y el elemento de interfaz de usuario será inaccesible para los usuarios con discapacidades.

## <a name="how-incorrect-naming-causes-problems"></a>Cómo causa problemas la nomenclatura incorrecta

Para ilustrar los problemas causados por una nomenclatura incorrecta de los elementos de la interfaz de usuario, considere el formulario de entrada de nombre que se muestra en la ilustración siguiente.

![ilustración de un formulario simple para escribir el nombre y los apellidos](images/incorrect-form.png)

Aunque los elementos de la interfaz de usuario con el formato parecen correctos, la implementación mediante programación no es correcta. Para un cliente Microsoft Active Accessibility, como un lector de pantalla, la propiedad [Name](name-property.md) del control de edición superior es "Last Name:" y la propiedad Name del control de edición inferior es una cadena vacía (""). El lector de pantalla leerá el control de edición superior como "Apellidos", aunque se espera que el usuario escriba el nombre. El lector de pantalla leerá el segundo control de edición como "sin nombre", por lo que el usuario no tendrá idea de qué escribir en el segundo control de edición. El lector de pantalla no puede ayudar al usuario a escribir datos en este formulario simple.

Otro problema con el formulario es que no se asignan teclas de método abreviado a ninguno de los controles de edición. El usuario se ve obligado a ir a los controles o usar el mouse.

En las secciones siguientes se explica el origen de estos problemas y se proporcionan instrucciones para corregirlos.

## <a name="how-msaa-gets-the-name-property"></a>Cómo obtiene MSAA la propiedad Name

Microsoft Active Accessibility la cadena [de propiedad Name](name-property.md) de ubicaciones diferentes según el tipo del elemento de interfaz de usuario. Para la mayoría de los elementos de la interfaz de usuario que tienen texto de ventana asociado, Microsoft Active Accessibility el texto de la ventana como la cadena de propiedad Name. Entre los ejemplos de este tipo de elemento de interfaz de usuario se incluyen controles como botones, elementos de menú e información sobre herramientas.

Para los siguientes controles, Microsoft Active Accessibility el texto de la ventana y, en su lugar, busca una etiqueta de texto estático (o etiqueta de cuadro de grupo) inmediatamente anterior al control en el orden de tabulación.

-   Cuadros combinados
-   Selectores de fecha y hora
-   Controles Editar y Editar enriquecidos
-   Controles de dirección IP
-   Cuadros de lista
-   Vistas de lista
-   Barras de progreso
-   Barras
-   Controles estáticos que tienen el estilo SS \_ ICON o SS \_ BITMAP
-   Barras de seguimiento
-   Vistas de árbol

Si los controles anteriores no van acompañados de etiquetas de texto estático o si las etiquetas no se implementan correctamente, Microsoft Active Accessibility puede proporcionar la propiedad [Name](name-property.md) correcta a las aplicaciones cliente.

La mayoría de los controles anteriores tienen realmente texto de ventana asociado. El editor de recursos genera automáticamente el texto de la ventana, que consta de una cadena genérica como "edit1" o "listbox3". Aunque los desarrolladores pueden reemplazar el texto de ventana generado por texto más significativo, la mayoría nunca lo hace. Dado que el texto de ventana generado no tiene ningún significado para el usuario, Microsoft Active Accessibility omite y usa la etiqueta de texto estático que lo acompaña en su lugar.

## <a name="how-to-find-and-correct-naming-problems"></a>Cómo buscar y corregir problemas de nomenclatura

En el formulario de entrada de nombre que se muestra en How Incorrect Naming Causes Problems ,la causa de los problemas es que el orden de tabulación de los controles es incorrecto. Examinar la interfaz de usuario con una herramienta de prueba como [Inspeccionar](inspect-objects.md) revelaría los problemas con la jerarquía de objetos. En la siguiente captura de pantalla se muestra la jerarquía de objetos rotos del formulario de entrada de nombre tal como aparece en Inspeccionar.

![captura de pantalla de la herramienta de inspección que muestra una jerarquía de objetos incorrecta del formulario de entrada de nombre](images/incorrect-object-hierarchy.png)

En la captura de pantalla anterior, observe que la jerarquía de objetos no coincide con la estructura de los controles tal como aparecen en la interfaz de usuario del formulario de entrada de nombre. Observe también [que Inspeccionar](inspect-objects.md) ha asignado el nombre incorrecto al elemento siguiente al último elemento (es el control de edición para escribir el nombre y debe tener el nombre "First Name:". Por último, observe que Inspeccionar no encontró un nombre para el último elemento (es el control de edición para escribir el apellido y debe tener un nombre de "Apellido:".

En el ejemplo siguiente se muestra el contenido del archivo de recursos para el formulario de entrada de nombre. Observe que el orden de tabulación no es coherente con la estructura lógica de los controles tal como aparecen en la interfaz de usuario. Observe también que no se especifican teclas de método abreviado para los dos controles de edición.

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

Para corregir los problemas con el formulario de entrada de nombre, se debe editar el archivo de recursos (.rc) para especificar métodos abreviados de teclado y los controles deben colocarse en el orden siguiente:

1.  Etiqueta de texto estático "&nombre:".
2.  Control de edición para escribir el nombre (IDC \_ EDIT1).
3.  Etiqueta de texto estático "&Apellidos:".
4.  Control de edición para escribir el apellido (IDC \_ EDIT2).
5.  Botón de inserción predeterminado "Aceptar".

En el ejemplo siguiente se muestra el archivo de recursos corregido para el formulario de entrada de nombre:

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

Para realizar correcciones en un archivo de recursos, puede editar el archivo directamente o puede usar la herramienta Orden de tabulación en Microsoft Visual Studio. Puede acceder a la herramienta Orden de tabulación Visual Studio presione CTRL+D o seleccione Orden de tabulación **en** el **menú** Formato.

Después de corregir y volver a generar la aplicación, la interfaz de usuario del formulario de entrada de nombres tendrá el mismo aspecto que antes. Sin embargo, Microsoft Active Accessibility proporcionará las propiedades de nombre correctas a las aplicaciones cliente y establecerá el foco correctamente cuando el usuario presione los métodos abreviados de teclado ALT+F o ALT+L. Además, [Inspeccionar](inspect-objects.md) mostrará la jerarquía de objetos correcta, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de la herramienta explorador accesible que muestra una jerarquía de objetos correcta del formulario de entrada de nombre](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Cómo nombrar correctamente una barra de seguimiento

Al definir una barra de seguimiento (o control deslizante), asegúrese de que la etiqueta de texto estático principal de la barra de seguimiento aparece delante de la barra de seguimiento y de que las etiquetas de texto estático para los intervalos mínimo y máximo aparecen después de la barra de seguimiento. Recuerde que Microsoft Active Accessibility la etiqueta de texto estático que precede inmediatamente a un control como la [propiedad Name](name-property.md) del control. Al colocar la etiqueta de texto estático principal inmediatamente antes de la barra de seguimiento y las demás etiquetas que hay después, se asegura de que Microsoft Active Accessibility proporciona la propiedad Name correcta a un cliente.

En la ilustración siguiente se muestra una barra de seguimiento típica con una etiqueta de texto estático principal denominada "Speed" y etiquetas de texto estático para los intervalos mínimo ("min") y máximo ("max").

![ilustración de un control trackbar que tiene una etiqueta principal y etiquetas para los intervalos mínimo y máximo](images/speed-trackbar.png)

En el ejemplo siguiente se muestra la manera correcta de definir una barra de seguimiento y sus etiquetas de texto estático en el archivo de recursos:

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Cómo usar etiquetas invisibles para dar nombre a controles

No siempre es posible o deseable tener una etiqueta visible para cada control. Por ejemplo, a veces, agregar etiquetas puede provocar cambios no deseados en la apariencia de la interfaz de usuario. En este caso, puede usar etiquetas invisibles. Microsoft Active Accessibility seguirá seleccionando el texto asociado a una etiqueta invisible, pero la etiqueta no aparecerá en la interfaz de usuario visual ni interferirá con ella.

Al igual que con las etiquetas visibles, una etiqueta invisible debe preceder inmediatamente al control en el orden de tabulación. Para hacer que una etiqueta sea invisible en un archivo de recursos (.rc), agregue o a la parte `NOT WS_VISIBLE` de estilo del control de texto `|~WS_VISIBLE` estático. Si usa el Editor de recursos en Visual Studio, puede establecer la propiedad Visible en False.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Cómo usar la anotación directa para especificar la propiedad Name

Los servidores proxy predeterminados incluidos en el componente de tiempo de ejecución Microsoft Active Accessibility, Oleacc.dll, proporcionan automáticamente un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos los controles Windows estándar. Si personaliza un control Windows estándar, los servidores proxy predeterminados hacen todo lo posible para proporcionar con precisión todas las propiedades **IAccessible** para el control personalizado. Debe probar exhaustivamente un control personalizado para asegurarse de que los servidores proxy predeterminados proporcionan valores de propiedad precisos y completos. Si las pruebas revelan valores de propiedad inexactos o incompletos, puede usar la técnica anotación dinámica denominada anotación directa para proporcionar valores de propiedad correctos y agregar los que faltan.

Tenga en cuenta que la anotación dinámica no es solo para los controles admitidos por los Microsoft Active Accessibility proxy. También puede usarlo para modificar o proporcionar propiedades para cualquier control que proporcione su propia [**implementación de IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Esta sección se centra en el uso de la anotación directa para proporcionar un valor correcto para la propiedad [Name](name-property.md) del [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un control . También puede usar la anotación directa para proporcionar otros valores de propiedades. Además, hay disponibles otras técnicas de anotación dinámica junto a la anotación directa, y las características y funcionalidades de la API de anotación dinámica se extienden mucho más allá de lo que se describe en esta sección. Para obtener más información sobre la anotación dinámica, vea [API de anotación dinámica.](dynamic-annotation-api.md)

### <a name="steps-for-annotating-the-name-property"></a>Pasos para anotar la propiedad Name

El uso de la anotación directa para cambiar [la propiedad Name](name-property.md) de un control implica los pasos siguientes.

1.  Incluya los siguientes archivos de encabezado:
    -   Initguid.h
    -   Oleacc.h

    > [!Note]  
    > Para definir GUID, debe incluir Initguid.h antes de Oleacc.h en el mismo archivo.

     

2.  Inicialice la biblioteca Del modelo de objetos componentes (COM) mediante una llamada a la [función CoInitializeEx,](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) normalmente durante el proceso de inicialización de la aplicación.
3.  Poco después de crear el control de destino (normalmente durante el mensaje [WM \_ INITDIALOG),](../dlgbox/wm-initdialog.md) cree una instancia del administrador de anotaciones y obtenga un puntero a su [**puntero IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
4.  Anote la [propiedad Name](name-property.md) del control de destino mediante el método [**IAccPropServices::SetHwndPropStr.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)

5.  Libere el [**puntero IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
6.  Antes de destruir el control de destino (normalmente al controlar el mensaje [WM \_ DESTROY),](../winmsg/wm-destroy.md) cree una instancia del administrador de anotaciones y obtenga un puntero a su [**interfaz IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
7.  Use el [**método IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) para borrar las anotaciones de la propiedad [Name](name-property.md) del control de destino.
8.  Libere el [**puntero IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
9.  Antes de que la aplicación se cierre (normalmente al procesar el [mensaje WM \_ DESTROY),](../winmsg/wm-destroy.md) libere la biblioteca COM mediante una llamada a [la función CoUninitialize.](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

La [**función IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) toma cinco parámetros. Los tres primeros,*hwnd*, *idObject* e *idChild,* se combinan para identificar el control. El cuarto parámetro, *idProp*, especifica el identificador de la propiedad que se va a cambiar. Para cambiar la [propiedad Name](name-property.md), establezca *idProp* en **PROPID ACC \_ \_ NAME**. (Para obtener una lista de otras propiedades que puede establecer a través de la anotación directa, vea [Usar anotación directa).](using-direct-annotation.md) El último parámetro de **SetHwndPropStr**, *str*, es la nueva cadena que se va a usar como la propiedad Name.

### <a name="example-of-annotating-the-name-property"></a>Ejemplo de anotación de la propiedad Name

En el código de ejemplo siguiente se muestra cómo usar la anotación directa para cambiar la [propiedad Name](name-property.md) del [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un control . Para que todo sea sencillo, en el ejemplo se usa una cadena codificada de forma fuerte ("Nuevo nombre de control") para establecer la propiedad Name. Las cadenas codificadas de forma hard-code no deben usarse en la versión final de la aplicación porque no se pueden localizar. En su lugar, cargue siempre cadenas desde el archivo de recursos. Además, en el ejemplo no se muestran las llamadas a las funciones [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [CoUninitialize.](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[API de anotación dinámica](dynamic-annotation-api.md)
</dt> <dt>

[Proporcionar la propiedad Name](providing-the-name-property.md)
</dt> <dt>

[Herramientas de prueba](testing-tools.md)
</dt> </dl>

 

 