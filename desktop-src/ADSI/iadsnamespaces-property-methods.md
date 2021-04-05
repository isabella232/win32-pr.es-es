---
title: Métodos de la propiedad IADsNamespaces (iAds. h)
description: Los métodos de propiedad de la interfaz IADsNamespaces obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803170"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="c9a85-105">Métodos de propiedad IADsNamespaces</span><span class="sxs-lookup"><span data-stu-id="c9a85-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="c9a85-106">Los métodos de propiedad de la interfaz [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtienen y establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9a85-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="c9a85-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c9a85-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c9a85-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9a85-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c9a85-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="c9a85-109">**DefaultContainer**</span></span>
<span data-ttu-id="c9a85-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c9a85-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c9a85-111">La propiedad **DefaultContainer** identifica un objeto contenedor base al que se puede enlazar y utilizar como punto de partida al examinar.</span><span class="sxs-lookup"><span data-stu-id="c9a85-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="c9a85-112">Estos datos se almacenan y recuperan del siguiente valor del registro.</span><span class="sxs-lookup"><span data-stu-id="c9a85-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="c9a85-113">ADSI define la propiedad **DefaultContainer** para proporcionar una forma rápida de obtener un puntero a un objeto de contenedor ADSI definido previamente.</span><span class="sxs-lookup"><span data-stu-id="c9a85-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="c9a85-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c9a85-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c9a85-115">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c9a85-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="c9a85-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9a85-116">Remarks</span></span>

<span data-ttu-id="c9a85-117">Los proveedores deben proporcionar esta propiedad por usuario.</span><span class="sxs-lookup"><span data-stu-id="c9a85-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="c9a85-118">El contenedor predeterminado se establece inmediatamente después de la invocación de **IADsNamespaces::p UT \_ DefaultContainer**.</span><span class="sxs-lookup"><span data-stu-id="c9a85-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="c9a85-119">No es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c9a85-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="c9a85-120">De hecho, el objeto de espacios de nombres proporcionado por el sistema devuelve **E \_ NOTIMPL** para el método **IADs. SetInfo** llamado en este objeto.</span><span class="sxs-lookup"><span data-stu-id="c9a85-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="c9a85-121">Cuando un contenedor es el objeto namespaces, una operación de enumeración siempre da como resultado una lista de objetos de espacio de nombres específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9a85-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="c9a85-122">Cuando se usa [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) para obtener un objeto de espacio de nombres, se omite el parámetro *bstrClass* .</span><span class="sxs-lookup"><span data-stu-id="c9a85-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="c9a85-123">Esto se debe a que el contenedor, es decir, el objeto namespaces, solo contiene un tipo de objeto, es decir, objetos de espacio de nombres específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9a85-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a85-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a85-124">Requirements</span></span>



| <span data-ttu-id="c9a85-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a85-125">Requirement</span></span> | <span data-ttu-id="c9a85-126">Value</span><span class="sxs-lookup"><span data-stu-id="c9a85-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a85-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a85-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a85-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9a85-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9a85-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a85-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a85-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9a85-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9a85-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9a85-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9a85-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a85-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c9a85-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9a85-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a85-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a85-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9a85-135">IID</span><span class="sxs-lookup"><span data-stu-id="c9a85-135">IID</span></span><br/>                      | <span data-ttu-id="c9a85-136">IID \_ IADsNamespaces se define como 28B96BA0-B330-11cf-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="c9a85-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c9a85-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9a85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a85-138">**IADsContainer. GetObject**</span><span class="sxs-lookup"><span data-stu-id="c9a85-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="c9a85-139">**IADsNamespaces**</span><span class="sxs-lookup"><span data-stu-id="c9a85-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="c9a85-140">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="c9a85-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





