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
# <a name="using-direct-annotation"></a><span data-ttu-id="00e59-103">Usar la anotación directa</span><span class="sxs-lookup"><span data-stu-id="00e59-103">Using Direct Annotation</span></span>

<span data-ttu-id="00e59-104">**Para utilizar la anotación directa para invalidar el valor de una propiedad**</span><span class="sxs-lookup"><span data-stu-id="00e59-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="00e59-105">Use la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear el objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="00e59-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="00e59-106">Llame a [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), pasando el **hWnd**, el ID. de objeto, el identificador secundario, la propiedad que se va a reemplazar y una [variante](/windows/win32/api/oaidl/ns-oaidl-variant) que contiene el nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="00e59-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="00e59-107">En este paso se anota el valor.</span><span class="sxs-lookup"><span data-stu-id="00e59-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="00e59-108">Liberar los punteros de interfaz y liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="00e59-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="00e59-109">En el ejemplo siguiente se muestra cómo anotar la propiedad [**role**](role-property.md) de un control de texto estático.</span><span class="sxs-lookup"><span data-stu-id="00e59-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


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



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="00e59-110">Propiedades admitidas al especificar un valor</span><span class="sxs-lookup"><span data-stu-id="00e59-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="00e59-111">Las siguientes propiedades de Microsoft Active Accessibility se pueden anotar al especificar un valor (donde el valor debe ser del tipo anotado) para la anotación directa.</span><span class="sxs-lookup"><span data-stu-id="00e59-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="00e59-112">Para invalidar o agregar una propiedad de automatización de la interfaz de usuario de Microsoft a un control, puede especificar el identificador de la propiedad de automatización de la interfaz de usuario en lugar del identificador de la propiedad de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="00e59-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="00e59-113">Para obtener una lista de los identificadores de automatización de la interfaz de usuario, vea [identificadores de propiedad](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="00e59-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="00e59-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00e59-114">Property</span></span>                      | <span data-ttu-id="00e59-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="00e59-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="00e59-116">nombre de la \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="00e59-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="00e59-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-117">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-118">Descripción de la definición del PROPID \_ \_</span><span class="sxs-lookup"><span data-stu-id="00e59-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="00e59-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-119">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-120">rol de PROPID \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="00e59-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="00e59-121">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="00e59-121">VT\_I4</span></span>   |
| <span data-ttu-id="00e59-122">Estado de la ACC de PROPID \_ \_</span><span class="sxs-lookup"><span data-stu-id="00e59-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="00e59-123">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="00e59-123">VT\_I4</span></span>   |
| <span data-ttu-id="00e59-124">ayuda de la ACC de PROPID \_ \_</span><span class="sxs-lookup"><span data-stu-id="00e59-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="00e59-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-125">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-126">KEYBOARDSHORTCUT de la \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="00e59-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="00e59-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-127">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-128">PROPID \_ ACC \_ DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="00e59-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="00e59-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-129">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-130">PROPID \_ ACC \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="00e59-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="00e59-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-131">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-132">ROLEMAP de la \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="00e59-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="00e59-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-133">VT\_BSTR</span></span> |
| <span data-ttu-id="00e59-134">STATEMAP de la \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="00e59-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="00e59-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="00e59-135">VT\_BSTR</span></span> |



 

 

 