---
title: Alternativas a la anotación dinámica
description: Alternativas a la anotación dinámica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149395"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativas a la anotación dinámica

Hay otras maneras de proporcionar compatibilidad de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personalizada para los elementos de la interfaz de usuario y, en algunos casos, son la solución correcta. Antes de la anotación dinámica, estas técnicas alternativas eran las únicas opciones disponibles para los desarrolladores. Incluyen la implementación de toda la interfaz **IAccessible** y las técnicas de programación.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementar toda la interfaz IAccessible

Una técnica alternativa consiste en implementar toda la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Este enfoque suele ser necesario para los controles personalizados o los elementos de interfaz de usuario radicalmente diferentes; sin embargo, los costos de desarrollo y pruebas son lo suficientemente significativos como para evitarlo a menos que sea realmente necesario. Si el objetivo es modificar una sola propiedad, el costo es difícil de justificar.

## <a name="programmatic-techniques"></a>Técnicas de programación

Otra opción consiste en usar técnicas de subclase y ajuste para modificar la información que se expone para una propiedad concreta. Esta es la técnica que la anotación dinámica va a reemplazar. Para reemplazar una propiedad única mediante el uso de subclases y el ajuste, el desarrollador debe realizar los siguientes pasos:

1.  Subclase del HWND del objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Interceptar el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para el valor de IParam/OBJID correcto.
3.  Reenvíe el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a la clase base mediante la función [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) . Si se devuelve cero, llame a [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); de lo contrario, llame a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) en el valor devuelto para obtener el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo del control.
4.  Cree una clase contenedora, que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y ajusta el puntero de la interfaz **IAccessible** devuelto en el paso anterior. Esta clase contenedora envía todos los métodos y propiedades al puntero de la interfaz **IAccessible** original, excepto los que se van a reemplazar. Esto implica la escritura de código de reenvío para todos los métodos y propiedades de la interfaz **IAccessible** , independientemente de cuántos se hayan invalidado realmente.

Además, los desarrolladores deben comprobar las condiciones siguientes:

-   El método o propiedad invalidados solo debe controlar los identificadores secundarios necesarios y reenviar todos los demás al puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.
-   El ajuste también debe reenviar las interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) y [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo si el objeto original las admite.
-   El recuento de referencias se debe administrar correctamente, especialmente si se admiten otras interfaces.
-   Los valores devueltos de [**IDispatch**](idispatch-interface.md) se deben controlar correctamente, especialmente con el método [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , al que se debe llamar con un puntero de interfaz a la interfaz contenedora, no un puntero a la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.

Estas técnicas requieren una cantidad considerable de trabajo, incluso si solo es necesario invalidar una o dos propiedades. La mayoría del código resultante está relacionada con la subclase y el ajuste, y solo una pequeña fracción proporciona realmente la información invalidada.

Sin embargo, hay escenarios en los que se necesitan estas técnicas. Por ejemplo, si está realizando cambios estructurales para crear un elemento de interfaz de usuario de marcador de posición, debe usar estas técnicas en lugar de la anotación dinámica.

## <a name="fixing-names-derived-from-labels"></a>Corregir nombres derivados de etiquetas

Algunos controles comunes de Microsoft Win32, como el control de cuadro de edición, casi siempre se usan con una etiqueta (una entrada LTEXT en el archivo de recursos) o un cuadro de grupo (GROUPBOX en el archivo de recursos). Microsoft Active Accessibility deriva automáticamente la propiedad Name del control de su etiqueta. Para estos controles, se omite el texto de la ventana (que se muestra en Microsoft Visual Studio como la propiedad Name o ID), porque normalmente se genera automáticamente y raramente es muy descriptivo. por ejemplo, "IDC \_ EDIT1".

Si la interfaz de usuario de la aplicación no está diseñada correctamente, es posible que Microsoft Active Accessibility no pueda establecer el nombre correctamente. Para asociar a un control, la etiqueta o el cuadro de grupo debe colocarse inmediatamente antes del control dinámico en el orden de tabulación.

El orden de tabulación se puede cambiar mediante la herramienta en Visual Studio (en el menú **formato** cuando el editor de recursos está abierto) o editando directamente el archivo de recursos.

En el ejemplo siguiente se muestra la descripción de un archivo de recursos de un cuadro de diálogo que contiene dos cuadros de edición con etiqueta.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



En este ejemplo, las etiquetas y los controles no aparecen en el orden de tabulación correcto. Como resultado, Microsoft Active Accessibility asigna el nombre "Last Name" al cuadro de edición First-Name y ningún nombre al cuadro de edición Last-Name.

En el ejemplo siguiente se muestra la lista de recursos correcta. Tenga en cuenta también que las teclas de método abreviado se han designado en las etiquetas.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



Cuando los controles tienen etiquetas adicionales, como los valores máximo y mínimo de una barra de control, estas etiquetas deben colocarse después del control en el orden de tabulación. La etiqueta principal del control debe aparecer inmediatamente antes del propio control.

## <a name="naming-controls-without-labels"></a>Asignar nombres a controles sin etiquetas

No siempre es posible o deseable tener una etiqueta visible para cada control. Sin embargo, puede proporcionar un nombre para el control agregando una etiqueta invisible. Como siempre, la etiqueta invisible debe preceder inmediatamente al control en el orden de tabulación.

Si usa el editor de recursos en Microsoft Visual Studio .NET, puede establecer la propiedad visible en false. Para hacer que la etiqueta sea invisible al editar el archivo de recursos (. RC), agregue no WS \_ visible o a la parte de estilo del control de etiqueta, como se muestra en el ejemplo siguiente.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Tenga en cuenta que cualquier tecla de método abreviado designada funciona aunque la etiqueta sea invisible.

 

 