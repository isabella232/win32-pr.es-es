---
title: Alternativas a la anotación dinámica
description: Alternativas a la anotación dinámica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070720"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativas a la anotación dinámica

Hay otras maneras de proporcionar compatibilidad [**personalizada con IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los elementos de la interfaz de usuario y, en algunos casos, son la solución correcta. Antes de la anotación dinámica, estas técnicas alternativas eran las únicas opciones disponibles para los desarrolladores. Incluyen la implementación de todas las técnicas de programación y la **interfaz IAccessible.**

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementar toda la interfaz IAccessible

Una técnica alternativa consiste en implementar toda la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Este enfoque suele ser necesario para controles personalizados o elementos de interfaz de usuario radicalmente diferentes. sin embargo, los costos de desarrollo y pruebas son lo suficientemente importantes como para evitarse a menos que sea realmente necesario. Si el objetivo es modificar una sola propiedad, el costo es difícil de justificar.

## <a name="programmatic-techniques"></a>Técnicas de programación

Otra opción consiste en usar subclases y técnicas de ajuste para modificar la información que se expone para una propiedad específica. Esta es la técnica que la anotación dinámica está diseñada para reemplazar. Para invalidar una sola propiedad mediante subclases y ajuste, el desarrollador debe realizar los pasos siguientes:

1.  Subclase el HWND del [**objeto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
2.  Intercepte [**el \_ mensaje GETOBJECT de WM**](wm-getobject.md) para el valor IParam/OBJID correcto.
3.  [**Reenvía el \_ mensaje GETOBJECT**](wm-getobject.md) de WM a la clase base mediante [*la función CallWndProc.*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) Si se devuelve cero, llame [**a CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); De lo contrario, [**llame a LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) en el valor devuelto para obtener el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo del control.
4.  Cree una clase contenedora, que implemente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y ajuste el puntero de interfaz **IAccessible** devuelto en el paso anterior. Esta clase contenedora envía todos los métodos y propiedades al puntero de interfaz **IAccessible** original, excepto los que se van a invalidar. Esto implica escribir código de reenvío para todas las 21 propiedades y métodos de la interfaz **IAccessible,** independientemente de cuántas se invaliden realmente.

Además, los desarrolladores deben comprobar las condiciones siguientes:

-   El método o propiedad invalidados solo debe controlar los identificadores secundarios necesarios y reenviar todos los demás al puntero de [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.
-   El ajuste también debe reenviar las interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) [**e IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo si el objeto original las admite.
-   El recuento de referencias debe controlarse correctamente, especialmente si se admiten otras interfaces.
-   Los valores devueltos de [**IDispatch**](idispatch-interface.md) deben controlarse correctamente, especialmente con el método [**ITypeInfo::Invoke,**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) al que se debe llamar con un puntero de interfaz a la interfaz contenedora, no con un puntero a la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.

Estas técnicas requieren una cantidad considerable de trabajo, incluso si solo es necesario invalidar una o dos propiedades. La mayoría del código resultante se refiere a las subclases y el ajuste, y solo una pequeña fracción proporciona realmente la información invalidada.

Sin embargo, hay escenarios en los que se necesitan estas técnicas. Por ejemplo, si va a realizar cambios estructurales para crear un elemento de interfaz de usuario de marcador de posición, debe usar estas técnicas en lugar de anotación dinámica.

## <a name="fixing-names-derived-from-labels"></a>Corregir nombres derivados de etiquetas

Algunos controles comunes de Microsoft Win32, como el control de cuadro de edición, casi siempre se usan con una etiqueta (una entrada LTEXT en el archivo de recursos) o un cuadro de grupo (GROUPBOX en el archivo de recursos). Microsoft Active Accessibility deriva automáticamente la propiedad name del control de su etiqueta. Para estos controles, el texto de la ventana (que se muestra en Microsoft Visual Studio como la propiedad Name o ID) se omite, ya que normalmente se genera automáticamente y rara vez es muy descriptivo; por ejemplo, "IDC \_ EDIT1".

Si la interfaz de usuario de la aplicación no está diseñada correctamente, Microsoft Active Accessibility podría no poder establecer el nombre correctamente. Para asociarse a un control, la etiqueta o el cuadro de grupo deben colocarse inmediatamente antes que el control dinámico en el orden de tabulación.

El orden de tabulación se puede cambiar mediante  la herramienta en Visual Studio (en el menú Formato cuando el editor de recursos está abierto) o editando directamente el archivo de recursos.

En el ejemplo siguiente se muestra la descripción de un archivo de recursos de un cuadro de diálogo que contiene dos cuadros de edición etiquetados.


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



En este ejemplo, las etiquetas y los controles no aparecen en el orden de tabulación correcto. Como resultado, Microsoft Active Accessibility el nombre "Apellidos" al cuadro de edición de nombre y ningún nombre en absoluto al cuadro de edición de apellidos.

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



Cuando los controles tienen etiquetas adicionales, como para los valores mínimo y máximo en una barra de seguimiento, estas etiquetas se deben colocar después del control en el orden de tabulación. La etiqueta principal del control debe aparecer inmediatamente antes del propio control.

## <a name="naming-controls-without-labels"></a>Asignar nombres a controles sin etiquetas

No siempre es posible o deseable tener una etiqueta visible para cada control. Sin embargo, todavía puede proporcionar un nombre para el control agregando una etiqueta invisible. Como siempre, la etiqueta invisible debe preceder inmediatamente al control en el orden de tabulación.

Si usa el Editor de recursos en Microsoft Visual Studio .NET, puede establecer la propiedad Visible en False. Para que la etiqueta sea invisible al editar el archivo de recursos (.rc), agregue NOT WS VISIBLE o a la parte de estilo del control de etiqueta, como se muestra \_ en el ejemplo siguiente.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Tenga en cuenta que cualquier tecla de método abreviado designada funciona aunque la etiqueta sea invisible.

 

 