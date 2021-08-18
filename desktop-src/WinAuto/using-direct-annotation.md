---
title: Usar anotación directa
description: Usar anotación directa
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8543b5aa4e6beb86b6119d13fe71ad45c1a34776e19095170cb48d8d9f48e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744890"
---
# <a name="using-direct-annotation"></a>Usar anotación directa

**Para usar la anotación directa para invalidar el valor de una propiedad**

1.  Use las [funciones CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear el [**objeto IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
2.  Llame a [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), pasando el **HWND**, el identificador de objeto, el identificador secundario, la propiedad que se va a invalidar y [un VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) que contiene el nuevo valor de la propiedad. Este paso anota el valor.
3.  Libere los punteros de interfaz y la memoria libre.

En el ejemplo siguiente se muestra cómo anotar la [**propiedad Role**](role-property.md) de un control de texto estático.


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

Las siguientes Microsoft Active Accessibility propiedades se pueden anotar al especificar un valor (donde el valor debe ser del tipo indicado) para la anotación directa. Para invalidar o agregar una propiedad Automatización de la interfaz de usuario de Microsoft a un control, puede especificar el identificador de propiedad Automatización de la interfaz de usuario en lugar del identificador Microsoft Active Accessibility propiedad. Para obtener una lista de Automatización de la interfaz de usuario identificadores de propiedad, vea [Identificadores de propiedad](uiauto-entry-propids.md).



| Propiedad                      | Tipo     |
|-------------------------------|----------|
| NOMBRE DE ACC DE PROPID \_ \_             | VT \_ BSTR |
| DESCRIPCIÓN DE \_ PROPID ACC \_      | VT \_ BSTR |
| PROPID \_ ACC \_ ROLE             | VT \_ I4   |
| PROPID \_ ACC \_ STATE            | VT \_ I4   |
| PROPID \_ ACC \_ HELP             | VT \_ BSTR |
| TECLADO \_ PROPID \_ ACCSHORTCUT | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR |
| MAPA DE \_ ROLES DE PROPID ACC \_          | VT \_ BSTR |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR |



 

 

 