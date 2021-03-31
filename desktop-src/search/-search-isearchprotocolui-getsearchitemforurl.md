---
description: Obtiene el elemento de búsqueda para los datos especificados. Se llama a este método una vez por cada dirección URL procesada por el recopilador y recupera un puntero al objeto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'ISearchProtocolUI:: GetSearchItemForUrl (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808948"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="6f394-104">ISearchProtocolUI:: GetSearchItemForUrl (método)</span><span class="sxs-lookup"><span data-stu-id="6f394-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="6f394-105">Obtiene el elemento de búsqueda para los datos especificados.</span><span class="sxs-lookup"><span data-stu-id="6f394-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="6f394-106">Se llama a este método una vez por cada dirección URL procesada por el recopilador y recupera un puntero al objeto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6f394-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f394-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f394-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="6f394-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f394-109">*pcwszURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f394-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f394-110">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="6f394-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="6f394-111">Puntero a una cadena Unicode terminada en datos null que contiene el elemento de búsqueda de la dirección URL a la que se obtiene acceso.</span><span class="sxs-lookup"><span data-stu-id="6f394-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="6f394-112">*pPropertyBag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f394-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f394-113">Tipo: \**IItemPropertyBag \** _</span><span class="sxs-lookup"><span data-stu-id="6f394-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="6f394-114">Puntero a un objeto [_ *IItemPropertyBag* \*](iitempropertybag.md) que contiene información sobre el elemento de búsqueda, incluidas las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f394-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="6f394-115">*ppSearchItem* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6f394-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6f394-116">Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6f394-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="6f394-117">Recibe la dirección de un puntero al objeto [**ISearchItem**](-search-isearchitem.md) creado por este método.</span><span class="sxs-lookup"><span data-stu-id="6f394-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="6f394-118">Este objeto contiene información sobre el elemento de búsqueda, como el nombre de archivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f394-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f394-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f394-119">Return value</span></span>

<span data-ttu-id="6f394-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f394-120">Type: **HRESULT**</span></span>

<span data-ttu-id="6f394-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6f394-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f394-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f394-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f394-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f394-123">Remarks</span></span>

<span data-ttu-id="6f394-124">El método **ISearchProtocolUI:: GetSearchItemForUrl** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="6f394-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="6f394-125">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**ISearchProtocolUI**](-search-isearchprotocolui.md) y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="6f394-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f394-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f394-126">Requirements</span></span>



| <span data-ttu-id="6f394-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f394-127">Requirement</span></span> | <span data-ttu-id="6f394-128">Value</span><span class="sxs-lookup"><span data-stu-id="6f394-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f394-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f394-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6f394-130">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f394-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f394-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f394-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6f394-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f394-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f394-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6f394-133">Redistributable</span></span><br/>          | <span data-ttu-id="6f394-134">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="6f394-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6f394-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f394-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f394-136">**ISearchProtocolUI**</span><span class="sxs-lookup"><span data-stu-id="6f394-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




