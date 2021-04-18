---
title: Exponer controles basados en controles del sistema
description: Exponer controles basados en controles del sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421176"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="970c3-103">Exponer controles basados en controles del sistema</span><span class="sxs-lookup"><span data-stu-id="970c3-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="970c3-104">Debe considerar el uso de alguna forma de anotación dinámica (directa, asignación de valores o servidor) antes de intentar la técnica descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="970c3-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="970c3-105">Para obtener más información, consulte [API de anotación dinámica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="970c3-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="970c3-106">En la mayoría de los casos, Microsoft Active Accessibility expone información sobre los controles con subclases o subclases.</span><span class="sxs-lookup"><span data-stu-id="970c3-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="970c3-107">La superclase y la creación de subclases permiten a los desarrolladores de aplicaciones crear un control personalizado con la funcionalidad básica de un control del sistema e incluir mejoras proporcionadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="970c3-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="970c3-108">Un control superclase tiene un nombre de clase de ventana diferente del control del sistema en el que se basa.</span><span class="sxs-lookup"><span data-stu-id="970c3-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="970c3-109">Un control subclase tiene el mismo nombre de clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="970c3-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="970c3-110">Para obtener más información acerca de la creación de subclases y subclases, consulte la documentación del kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="970c3-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="970c3-111">Dado que Microsoft Active Accessibility expone información sobre los controles proporcionados por el sistema, Microsoft Active Accessibility expone el control modificado a menos que un control superclase o subclase sea significativamente diferente del control base.</span><span class="sxs-lookup"><span data-stu-id="970c3-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="970c3-112">Para determinar si el control modificado es accesible, los desarrolladores de aplicaciones deben usar utilidades como [inspeccionar](inspect-objects.md) y el [monitor de eventos accesible](accessible-event-watcher.md) para comparar el comportamiento del control modificado con el control base.</span><span class="sxs-lookup"><span data-stu-id="970c3-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="970c3-113">Si después de usar estas utilidades determina que el control modificado no es accesible, debe tratar el control como cualquier otro control personalizado.</span><span class="sxs-lookup"><span data-stu-id="970c3-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="970c3-114">El control debe desencadenar eventos y el procedimiento de ventana de la aplicación debe responder al mensaje de [**WM \_ GETOBJECT**](wm-getobject.md)proporcionando una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que las aplicaciones cliente usan para obtener información sobre el control.</span><span class="sxs-lookup"><span data-stu-id="970c3-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="970c3-115">CreateStdAccessibleProxy y CreateStdAccessibleObject</span><span class="sxs-lookup"><span data-stu-id="970c3-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="970c3-116">Si todas o la mayoría de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del control modificado son las mismas que el control base, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) o [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) para simplificar la implementación de la interfaz **IAccessible** del control.</span><span class="sxs-lookup"><span data-stu-id="970c3-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="970c3-117">Al superponer o crear subclases de un control accesible, tenga en cuenta que el objeto recuperado por la función [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) puede implementar algo más que simplemente la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="970c3-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="970c3-118">Puede incluir otras interfaces como [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span><span class="sxs-lookup"><span data-stu-id="970c3-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="970c3-119">Es posible que tenga que ajustar estas interfaces adicionales para conservar la compatibilidad de accesibilidad proporcionada por la implementación original del control.</span><span class="sxs-lookup"><span data-stu-id="970c3-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="970c3-120">Las funciones [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) y [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperan un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el control del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="970c3-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="970c3-121">La diferencia entre estas funciones es que **CreateStdAccessibleObject** usa el nombre de clase de ventana Obtenido de su parámetro *hWnd* , mientras que **CreateStdAccessibleProxy** usa el nombre de clase de ventana especificado en su parámetro *szClassName* .</span><span class="sxs-lookup"><span data-stu-id="970c3-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="970c3-122">Por consiguiente, si decide usar estas funciones, use **CreateStdAccessibleProxy** para exponer información acerca de los controles superclases y, a su vez, puede usarlos con controles de subclase.</span><span class="sxs-lookup"><span data-stu-id="970c3-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="970c3-123">Después de obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al control del sistema, utilice el puntero en la implementación de la interfaz **IAccessible** para el control modificado.</span><span class="sxs-lookup"><span data-stu-id="970c3-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="970c3-124">Si una propiedad o un método para el control modificado es el mismo que el control base, use el puntero **IAccessible** para devolver la información proporcionada por el control base.</span><span class="sxs-lookup"><span data-stu-id="970c3-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="970c3-125">Si una propiedad del control modificado es diferente del control base, invalide la propiedad del control base.</span><span class="sxs-lookup"><span data-stu-id="970c3-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="970c3-126">En el ejemplo siguiente, **CAccCustomButton** es la clase definida por la aplicación derivada de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="970c3-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="970c3-127">La variable miembro **m \_ pAccDefaultButton** es un puntero a una interfaz **IAccessible** que se recuperó de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante el procedimiento de inicialización para el control.</span><span class="sxs-lookup"><span data-stu-id="970c3-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="970c3-128">En este ejemplo, la propiedad **role** del control personalizado es la misma que la propiedad **role** del control del sistema, por lo que se devuelve la propiedad **role** del control base.</span><span class="sxs-lookup"><span data-stu-id="970c3-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="970c3-129">Sin embargo, la propiedad **Description** es diferente de la del control base, por lo que esta propiedad se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="970c3-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="970c3-130">Para obtener más información sobre las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de los controles del sistema, vea [Apéndice A: referencia de elementos de la interfaz de usuario compatibles](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="970c3-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 