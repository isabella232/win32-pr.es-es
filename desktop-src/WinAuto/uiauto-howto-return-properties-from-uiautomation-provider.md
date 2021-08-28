---
title: Cómo devolver propiedades de un proveedor Automatización de la interfaz de usuario datos
description: Este tema contiene código de ejemplo que muestra cómo un proveedor de Automatización de la interfaz de usuario microsoft devuelve las propiedades de un elemento de interfaz de usuario a las aplicaciones cliente.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1284e2969d726006b4f8a8b0b6b3e63a7e421a14fb688dae5cbf8b8aa53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859465"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Cómo devolver propiedades de un proveedor Automatización de la interfaz de usuario datos

Este tema contiene código de ejemplo que muestra cómo un proveedor de Automatización de la interfaz de usuario microsoft devuelve las propiedades de un elemento de interfaz de usuario a las aplicaciones cliente.

Para recuperar un valor de propiedad del proveedor, Automatización de la interfaz de usuario llama a la implementación de un proveedor del método [**IRawElementProviderSimple::GetPropertyValue,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) pasando el identificador de la propiedad que se va a recuperar y un puntero a una estructura [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Si el proveedor admite la propiedad especificada, copia el tipo de datos y el valor de la propiedad en la **estructura VARIANT.** Si no se admite la propiedad , el proveedor establece el **miembro vt** de la **estructura VARIANT** en VT \_ EMPTY.


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

**Conceptual**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Temas de ayuda para proveedores de Automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 