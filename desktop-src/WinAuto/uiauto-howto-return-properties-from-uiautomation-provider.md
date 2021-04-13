---
title: Cómo devolver propiedades de un proveedor de automatización de la interfaz de usuario
description: Este tema contiene código de ejemplo que muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft devuelve las propiedades de un elemento de la interfaz de usuario a las aplicaciones cliente.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420771"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Cómo devolver propiedades de un proveedor de automatización de la interfaz de usuario

Este tema contiene código de ejemplo que muestra cómo un proveedor de automatización de la interfaz de usuario de Microsoft devuelve las propiedades de un elemento de la interfaz de usuario a las aplicaciones cliente.

Para recuperar un valor de propiedad del proveedor, la automatización de la interfaz de usuario llama a la implementación de un proveedor del método [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , pasando el identificador de la propiedad que se va a recuperar y un puntero a una estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Si el proveedor es compatible con la propiedad especificada, copia el tipo de datos y el valor de la propiedad en la estructura de **variante** . Si no se admite la propiedad, el proveedor establece el miembro **VT** de la estructura **Variant** en VT \_ vacío.


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Temas de procedimientos para los proveedores de automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 