---
title: Cómo se usan los identificadores secundarios en los parámetros
description: En este tema se describen los parámetros de entrada, los parámetros de salida y los casos especiales para interpretar los identificadores secundarios devueltos por los métodos IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420961"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Cómo se usan los identificadores secundarios en los parámetros

En este tema se describen los parámetros de entrada, los parámetros de salida y los casos especiales para interpretar los identificadores secundarios devueltos por los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="input-parameters"></a>Parámetros de entrada

Muchas de las funciones de Microsoft Active Accessibility y la mayoría de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) toman una estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) como parámetro de entrada. Para la mayoría de las propiedades **IAccessible** , este parámetro permite a los desarrolladores de cliente especificar si desean información sobre el propio objeto o sobre uno de los elementos simples del objeto.

Microsoft Active Accessibility proporciona la constante **CHILDID \_ Self** para indicar que se necesita información sobre el propio objeto. Para obtener información sobre un elemento simple, los desarrolladores de cliente especifican su identificador secundario en el parámetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Al inicializar un parámetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , asegúrese de especificar **VT \_ I4** en el miembro de **VT** , además de especificar el valor de identificador secundario (o **CHILDID \_ Self**) en el miembro **lVal** .

Por ejemplo, para obtener el nombre de un objeto, y no uno de los elementos secundarios del objeto, inicialice la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) para el primer parámetro de [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ Self** en el miembro **lVal** y **VT \_ I4** en el miembro **VT** ) y, a continuación, llame a **IAccessible:: get \_ accName**.

## <a name="output-parameters"></a>Parámetros de salida

Varias funciones y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) tienen un [](/windows/win32/api/oaidl/ns-oaidl-variant) \* parámetro de salida Variant que contiene un identificador secundario o un puntero de interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) a un objeto secundario. Hay diferentes pasos que un cliente debe realizar en función de si reciben un identificador secundario de **VT \_ I4** (elemento simple) o un puntero de interfaz **IDispatch** con **CHILDID \_ Self** (objeto completo). Al seguir estos pasos, se proporcionará un puntero de interfaz **IAccessible** y un identificador secundario que juntos permiten a los clientes usar los métodos y las propiedades de **IAccessible** . Estos pasos se aplican a los métodos [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)y [**Get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . También se aplican a las funciones de cliente [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)y [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

En la tabla siguiente se enumeran los posibles resultados devueltos y los pasos de procesamiento posteriores necesarios para que los clientes tengan un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario.



| Resultado devuelto                                      | Procesamiento posterior para el valor devuelto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Puntero de interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Es un objeto completo. Llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para tener acceso al puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Use el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con **CHILDID \_ Self** para tener acceso a los métodos y propiedades de **IAccessible** .<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_ID. secundario de VT I4                                      | Llame a [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) con el identificador secundario para ver si tiene un puntero de interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . Si obtiene un puntero de interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , úselo con **CHILDID \_ Self** para tener acceso a los métodos y propiedades de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Si se produce un error en la llamada a [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) , tiene un elemento simple. Use el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original (el que usó en la llamada al método o la función mencionada anteriormente) con el identificador secundario **VT \_ I4** que devolvió la llamada.<br/> |



 

Antes de poder usar un parámetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , debe inicializarlo mediante una llamada a la función [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) del modelo de objetos componentes (com). Cuando termine con la estructura, llame a [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) para liberar la memoria reservada para esa **variante**.

## <a name="special-cases"></a>Casos especiales

Existen excepciones a las instrucciones de la tabla anterior, como cuando el método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) devuelve un identificador secundario. Los servidores deben devolver una interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) si el elemento secundario es un objeto accesible. Si **IAccessible:: accHitTest** devuelve un identificador secundario, el elemento secundario es un elemento simple.

Además, hay casos especiales para [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Para obtener más información, vea **IAccessible:: accNavigate** y [navegación espacial y lógica](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Interfaz IDispatch](idispatch-interface.md)
</dt> <dt>

[VARIANT (estructura)](variant-structure.md)
</dt> </dl>

 

