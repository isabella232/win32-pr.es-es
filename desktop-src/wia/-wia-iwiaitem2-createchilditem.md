---
description: Cree un nuevo elemento secundario. Agrega objetos IWiaItem2 al árbol IWiaItem2 de un dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2:: CreateChildItem (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716049"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="1eca0-104">IWiaItem2:: CreateChildItem (método)</span><span class="sxs-lookup"><span data-stu-id="1eca0-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="1eca0-105">Cree un nuevo elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="1eca0-105">Create a new child item.</span></span> <span data-ttu-id="1eca0-106">Agrega objetos [**IWiaItem2**](-wia-iwiaitem2.md) al árbol **IWiaItem2** de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1eca0-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eca0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1eca0-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="1eca0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1eca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eca0-109">*lItemFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eca0-110">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="1eca0-110">Type: **LONG**</span></span>

<span data-ttu-id="1eca0-111">Especifica el tipo de elemento de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="1eca0-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="1eca0-112">Vea [**marcas de tipo de elemento de WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1eca0-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1eca0-113">*lCreationFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eca0-114">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="1eca0-114">Type: **LONG**</span></span>

<span data-ttu-id="1eca0-115">Especifica cómo crear el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="1eca0-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1eca0-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="1eca0-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1eca0-117">Establezca los valores predeterminados para las propiedades del elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="1eca0-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="1eca0-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copiar \_ \_ \_ Valores de propiedad primarios** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="1eca0-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="1eca0-119">Copie los valores de todas las propiedades de lectura y escritura del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1eca0-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1eca0-120">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eca0-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1eca0-121">Type: **BSTR**</span></span>

<span data-ttu-id="1eca0-122">Especifica el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="1eca0-122">Specifies the item name.</span></span> <span data-ttu-id="1eca0-123">Este nombre se anexa al final del nombre del elemento primario para generar el nombre completo del elemento.</span><span class="sxs-lookup"><span data-stu-id="1eca0-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="1eca0-124">*ppIWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eca0-125">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1eca0-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="1eca0-126">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que establece el método **IWiaItem2:: CreateChildItem** .</span><span class="sxs-lookup"><span data-stu-id="1eca0-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eca0-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1eca0-127">Return value</span></span>

<span data-ttu-id="1eca0-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1eca0-128">Type: **HRESULT**</span></span>

<span data-ttu-id="1eca0-129">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1eca0-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1eca0-130">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1eca0-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eca0-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1eca0-131">Remarks</span></span>

<span data-ttu-id="1eca0-132">Algunos dispositivos de hardware WIA 2,0 permiten a las aplicaciones crear nuevos elementos en el árbol [**IWiaItem2**](-wia-iwiaitem2.md) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1eca0-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="1eca0-133">Las aplicaciones deben probar los dispositivos para ver si admiten esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="1eca0-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="1eca0-134">Use la \_ interfaz IEnumWIA dev \_ Caps para enumerar las capacidades del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="1eca0-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="1eca0-135">Si el dispositivo permite la creación de nuevos elementos en el árbol [**IWiaItem2**](-wia-iwiaitem2.md) , al invocar **IWiaItem2:: CreateChildItem** se crea un nuevo objeto **IWiaItem2** que es un elemento secundario del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="1eca0-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="1eca0-136">Pasa un puntero al nuevo nodo a la aplicación a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="1eca0-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="1eca0-137">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="1eca0-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="1eca0-138">Si *lCreationFlags* es Copy \_ Parent \_ Property \_ Values y *lItemFlags* es cero, la función devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1eca0-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eca0-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1eca0-139">Requirements</span></span>



| <span data-ttu-id="1eca0-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eca0-140">Requirement</span></span> | <span data-ttu-id="1eca0-141">Value</span><span class="sxs-lookup"><span data-stu-id="1eca0-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1eca0-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1eca0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1eca0-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1eca0-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1eca0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1eca0-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1eca0-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1eca0-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1eca0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eca0-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eca0-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1eca0-148">IDL</span><span class="sxs-lookup"><span data-stu-id="1eca0-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1eca0-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1eca0-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
