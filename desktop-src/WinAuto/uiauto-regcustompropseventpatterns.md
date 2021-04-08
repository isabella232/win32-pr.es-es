---
title: Registrar propiedades, eventos y patrones de control personalizados
description: Antes de que se pueda usar una propiedad personalizada, un evento o un patrón de control, tanto el proveedor como el cliente deben registrar la propiedad, el evento o el patrón de control en tiempo de ejecución.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automatización de la interfaz de usuario, propiedades personalizadas
- Automatización de la interfaz de usuario, información general sobre eventos
- UI Automation, información general sobre los patrones de control
- Automatización de la interfaz de usuario, registrar propiedades personalizadas
- Automatización de la interfaz de usuario, registrar eventos
- Automatización de la interfaz de usuario, registrar patrones de control
- propiedades personalizadas, registrar
- eventos, registrar
- patrones de control, registrar
- registrar, propiedades personalizadas
- registrar, eventos
- registrar, patrones de control
- patrones de control, personalizados
- patrones de control, implementar personalizados
- implementar patrones de control personalizados
- patrones de control personalizados
- contenedores de cliente
- Controladores de patrón
- implementar controladores de patrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078192"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Registrar propiedades, eventos y patrones de control personalizados

Antes de que se pueda usar una propiedad personalizada, un evento o un patrón de control, tanto el proveedor como el cliente deben registrar la propiedad, el evento o el patrón de control en tiempo de ejecución. El registro es efectivo globalmente dentro de un proceso de aplicación y permanece efectivo hasta que se cierra el proceso o hasta que se libera el último objeto de elemento de automatización de la interfaz de usuario de Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) o [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) dentro del proceso.

El registro implica pasar un GUID a la automatización de la interfaz de usuario, junto con información detallada sobre la propiedad personalizada, el evento o el patrón de control. Si se intenta registrar el mismo GUID una segunda vez con la misma información, se realizará correctamente, pero se producirá un error al intentar registrar el mismo GUID una segunda vez pero con información diferente (por ejemplo, una propiedad personalizada de un tipo diferente). En el futuro, si se acepta la especificación personalizada y se integra en el núcleo de automatización de la interfaz de usuario, la automatización de la interfaz de usuario validará la información de registro personalizada y usará el código ya registrado en lugar de la implementación del marco "oficial", con lo que se minimizan los problemas de compatibilidad de aplicaciones. No se pueden quitar las propiedades, los eventos o los patrones de control que ya están registrados.

Este tema contiene las siguientes secciones:

-   [Registrar eventos y propiedades personalizadas](#registering-custom-properties-and-events)
-   [Implementar patrones de control personalizados](#implementing-custom-control-patterns)
    -   [Contenedor de cliente y controlador de patrón](#the-client-wrapper-and-the-pattern-handler)
    -   [Implementar el contenedor de cliente](#implementing-the-client-wrapper)
    -   [Implementar el controlador de patrón](#implementing-the-pattern-handler)
    -   [Registrar un patrón de control personalizado](#registering-a-custom-control-pattern)
    -   [Ejemplo de implementación de un patrón de control personalizado](#example-implementation-of-a-custom-control-pattern)
-   [Temas relacionados](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Registrar eventos y propiedades personalizadas

El registro de una propiedad o un evento personalizado permite al proveedor y al cliente obtener un identificador para la propiedad o evento, que se puede pasar a los distintos métodos de API que toman los identificadores como parámetros.

Para registrar una propiedad o un evento:

1.  Defina un GUID para la propiedad o el evento personalizado.
2.  Rellene una estructura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) con información sobre la propiedad o el evento, incluido el GUID y una cadena no localizable que contenga el nombre de la propiedad o el evento personalizado. Las propiedades personalizadas también requieren el tipo de datos de la propiedad que se va a especificar, por ejemplo, si la propiedad contiene un entero o una cadena. El tipo de datos debe ser uno de los siguientes tipos especificados por la enumeración [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . No se admiten otros tipos de datos para las propiedades personalizadas.
    -   **UIAutomationType \_ bool**
    -   **UIAutomationType \_ doble**
    -   **\_Elemento UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **\_Punto UIAutomationType**
    -   **\_Cadena UIAutomationType**
3.  Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) y recuperar un puntero a la interfaz [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) del objeto.
4.  Llame al método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) y pase la dirección de la estructura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o la estructura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .

El método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) devuelve un identificador de propiedad o un identificador de evento que una aplicación puede pasar a cualquier método de automatización de la interfaz de usuario que tome dicho identificador como parámetro. Por ejemplo, puede pasar un identificador de propiedad registrado al método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) o al método [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .

En el ejemplo siguiente se muestra cómo registrar una propiedad personalizada.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Los identificadores de propiedad y evento recuperados por los métodos [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) y [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) solo son válidos en el contexto de la aplicación que los recupera y solo mientras dure la duración de la aplicación. Los métodos de registro pueden devolver valores enteros diferentes para el mismo GUID cuando se llama a través de distintas instancias en tiempo de ejecución de la misma aplicación.

No hay ningún método que anule el registro de una propiedad o evento personalizado. En su lugar, se anula el registro de forma implícita cuando se libera el último objeto de automatización de la interfaz de usuario.

> [!IMPORTANT]
> Si el código es un cliente de Microsoft Active Accessibility (MSAA), debe llamar a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) al cambiar el valor de una propiedad personalizada.

 

## <a name="implementing-custom-control-patterns"></a>Implementar patrones de control personalizados

Un patrón de control personalizado no se incluye en la API de automatización de la interfaz de usuario, pero lo proporciona un tercero en tiempo de ejecución. Los desarrolladores de aplicaciones de cliente y de proveedor deben funcionar juntos para definir un patrón de control personalizado, incluidos los métodos, las propiedades y los eventos que el patrón de control admitirá. Después de definir el patrón de control, tanto el cliente como el proveedor deben implementar objetos auxiliares del modelo de objetos componentes (COM), junto con código para registrar el patrón de control en tiempo de ejecución. Un patrón de control personalizado requiere la implementación de dos objetos COM: un contenedor de cliente y un controlador de patrón.

> [!Note]  
> En los ejemplos de los temas siguientes se muestra cómo implementar un patrón de control personalizado que duplique la funcionalidad del patrón de control [Value](uiauto-implementingvalue.md) existente. Estos ejemplos son solo con fines informativos. Un patrón de control personalizado real debe proporcionar funcionalidad que no está disponible en los patrones de control de automatización de la interfaz de usuario estándar.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Contenedor de cliente y controlador de patrón

El contenedor de cliente implementa la API que usa el cliente para recuperar las propiedades y llamar a los métodos expuestos por el patrón de control personalizado. La API se implementa como una interfaz COM que pasa todas las solicitudes de propiedades y llamadas a métodos al núcleo de automatización de la interfaz de usuario, que luego calcula las referencias de las solicitudes y llamadas al proveedor.

El código que registra un patrón de control personalizado debe proporcionar un generador de clases que la automatización de la interfaz de usuario puede usar para crear instancias del objeto contenedor de cliente. Cuando un patrón de control personalizado se registra correctamente, la automatización de la interfaz de usuario devuelve un puntero de la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) que usa el cliente para reenviar solicitudes de propiedades y llamadas a métodos al núcleo de automatización de la interfaz de usuario.

En el lado del proveedor, el núcleo de automatización de la interfaz de usuario toma las solicitudes de propiedades y las llamadas a métodos desde el cliente y las pasa al objeto de controlador de patrón. A continuación, el controlador de patrón llama a los métodos adecuados en la interfaz del proveedor para el patrón de control personalizado.

El código que registra un patrón de control personalizado crea el objeto de controlador de patrón y, al registrar el patrón de control, proporciona automatización de la interfaz de usuario con un puntero a la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto.

En el diagrama siguiente se muestra cómo una solicitud de propiedad de cliente o una llamada de método fluyen desde el contenedor de cliente, a través de los componentes principales de UI Automation hasta el controlador de patrón y, a continuación, a la interfaz del proveedor.

![diagrama que muestra el flujo del contenedor del cliente al controlador y al proveedor del patrón](images/custompatternsupport.jpg)

Los objetos que implementan las interfaces de contenedor de cliente y controlador de patrón deben ser de subprocesamiento libre. Además, el núcleo de automatización de la interfaz de usuario debe poder llamar a los objetos directamente sin ningún código de serialización intermedio.

### <a name="implementing-the-client-wrapper"></a>Implementar el contenedor de cliente

El contenedor de cliente es un objeto que expone una interfaz IXxxPattern que el cliente usa para solicitar propiedades y llamar a métodos admitidos por el patrón de control personalizado. La interfaz está formada por un par de métodos de "captador" para cada propiedad admitida (get \_ CurrentXxx y Get \_ CachedXxx Method) y un método "Caller" para cada método admitido. Cuando se crea una instancia del objeto, el constructor de objeto recibe un puntero a la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , que se implementa mediante el núcleo de automatización de la interfaz de usuario. Los métodos de la interfaz IXxxPattern usan los métodos [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) y [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) para reenviar las solicitudes de propiedades y las llamadas de método al núcleo de automatización de la interfaz de usuario.

En el ejemplo siguiente se muestra cómo implementar un objeto contenedor de cliente para un patrón de control personalizado simple que admite una sola propiedad. Para obtener un ejemplo más complejo, vea [ejemplo de implementación de un patrón de control personalizado](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Implementar el controlador de patrón

El controlador de patrón es un objeto que implementa la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) . Esta interfaz tiene dos métodos: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) y [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). El núcleo de la automatización de la interfaz de usuario llama al método **CreateClientWrapper** y recibe un puntero a la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) . **CreateClientWrapper** responde creando instancias del objeto contenedor de cliente y pasando el puntero de la interfaz **IUIAutomationPatternInstance** al constructor contenedor de cliente.

El núcleo de automatización de la interfaz de usuario usa el método [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) para pasar las solicitudes de propiedad y las llamadas de método a la interfaz del proveedor para el patrón de control personalizado. Los parámetros incluyen un puntero a la interfaz del proveedor, el índice de base cero del captador de propiedad o método al que se llama, y una matriz de estructuras [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) que contienen los parámetros que se van a pasar al proveedor. El controlador de patrón responde comprobando el parámetro de índice para determinar el método de proveedor al que llamar y, a continuación, llama a la interfaz del proveedor, pasando los parámetros contenidos en las estructuras **UIAutomationParameter** .

Se crea una instancia del objeto de controlador de patrón mediante el mismo código que registra el patrón de control personalizado antes de que se registre el patrón de control. El código debe pasar el puntero de la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto de controlador de patrón al núcleo de automatización de la interfaz de usuario en el momento del registro.

En el ejemplo siguiente se muestra cómo implementar un objeto de controlador de patrón para un patrón de control personalizado simple que admite una sola propiedad. Para obtener un ejemplo más complejo, vea [ejemplo de implementación de un patrón de control personalizado](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Registrar un patrón de control personalizado

Antes de que se pueda usar, el proveedor y el cliente deben registrar un patrón de control personalizado. El registro proporciona el núcleo de automatización de la interfaz de usuario con información detallada sobre el patrón de control y proporciona al proveedor o al cliente el identificador de patrón de control, así como los identificadores de las propiedades y los eventos que admite el patrón de control. En el lado del proveedor, se debe registrar el patrón de control personalizado antes de que el control asociado administre el mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) o al mismo tiempo.

Al registrar un patrón de control personalizado, el proveedor o el cliente proporciona la siguiente información:

-   GUID del patrón de control personalizado.
-   Una cadena no localizable que contiene el nombre del patrón de control personalizado.
-   GUID de la interfaz del proveedor que admite el patrón de control personalizado.
-   GUID de la interfaz de cliente que admite el patrón de control personalizado.
-   Matriz de estructuras [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) que describen las propiedades admitidas por el patrón de control personalizado. Para cada propiedad, se deben especificar el GUID, el nombre de la propiedad y el tipo de datos.
-   Matriz de estructuras [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) que describen los métodos admitidos por el patrón de control personalizado. Para cada método, la estructura incluye la información siguiente: el nombre del método, un recuento de parámetros, una lista de tipos de datos de parámetros y una lista de los nombres de parámetro.
-   Matriz de estructuras [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) que describen los eventos generados por el patrón de control personalizado. Para cada evento, debe especificarse el GUID y el nombre del evento.
-   Dirección de la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto de controlador de patrón que hace que el patrón de control personalizado esté disponible para los clientes.

Para registrar el patrón de control personalizado, el código de cliente o proveedor debe realizar los siguientes pasos:

1.  Rellene una estructura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) con la información anterior.
2.  Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) y recuperar un puntero a la interfaz [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) del objeto.
3.  Llame al método [**IUIAutomationRegistrar:: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , pasando la dirección de la estructura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .

El método [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) devuelve un identificador de patrón de control, junto con una lista de identificadores de propiedades e identificadores de eventos. Una aplicación puede pasar estos identificadores a cualquier método de automatización de la interfaz de usuario que tome dicho identificador como parámetro. Por ejemplo, puede pasar un identificador de patrón registrado al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) para recuperar un puntero a la interfaz del proveedor para el patrón de control.

No hay ningún método que anule el registro de un patrón de control personalizado. En su lugar, se anula el registro de forma implícita cuando se libera el último objeto de automatización de la interfaz de usuario.

Para obtener un ejemplo en el que se muestra cómo registrar un patrón de control personalizado, consulte la sección siguiente.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Ejemplo de implementación de un patrón de control personalizado

Esta sección contiene código de ejemplo que muestra cómo implementar los objetos contenedor de cliente y controlador de patrón para un patrón de control personalizado. En el ejemplo se implementa un patrón de control personalizado basado en el patrón de control [Value](uiauto-implementingvalue.md) .


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Diseñar propiedades, eventos y patrones de control personalizados](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 