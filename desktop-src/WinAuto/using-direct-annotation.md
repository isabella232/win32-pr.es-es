---
title: Usar la anotación directa
description: Usar la anotación directa
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359149"
---
# <a name="using-direct-annotation"></a>Usar la anotación directa

**Para utilizar la anotación directa para invalidar el valor de una propiedad**

1.  Use la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear el objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
2.  Llame a [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), pasando el **hWnd**, el ID. de objeto, el identificador secundario, la propiedad que se va a reemplazar y una [variante](/windows/win32/api/oaidl/ns-oaidl-variant) que contiene el nuevo valor de la propiedad. En este paso se anota el valor.
3.  Liberar los punteros de interfaz y liberar memoria.

En el ejemplo siguiente se muestra cómo anotar la propiedad [**role**](role-property.md) de un control de texto estático.


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a>Propiedades admitidas al especificar un valor

Las siguientes propiedades de Microsoft Active Accessibility se pueden anotar al especificar un valor (donde el valor debe ser del tipo anotado) para la anotación directa. Para invalidar o agregar una propiedad de automatización de la interfaz de usuario de Microsoft a un control, puede especificar el identificador de la propiedad de automatización de la interfaz de usuario en lugar del identificador de la propiedad de Microsoft Active Accessibility. Para obtener una lista de los identificadores de automatización de la interfaz de usuario, vea [identificadores de propiedad](uiauto-entry-propids.md).



| Propiedad                      | Tipo     |
|-------------------------------|----------|
| nombre de la \_ ACC \_             | VT \_ BSTR |
| Descripción de la definición del PROPID \_ \_      | VT \_ BSTR |
| rol de PROPID \_ ACC \_             | VT \_ I4   |
| Estado de la ACC de PROPID \_ \_            | VT \_ I4   |
| ayuda de la ACC de PROPID \_ \_             | VT \_ BSTR |
| KEYBOARDSHORTCUT de la \_ ACC \_ | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR |
| ROLEMAP de la \_ ACC \_          | VT \_ BSTR |
| STATEMAP de la \_ ACC \_         | VT \_ BSTR |



 

 

 