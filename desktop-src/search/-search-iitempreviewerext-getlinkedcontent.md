---
description: Permite la extensión a contenido enriquecido para una propiedad.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'IItemPreviewerExt:: GetLinkedContent (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720334"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="ba3ae-103">IItemPreviewerExt:: GetLinkedContent (método)</span><span class="sxs-lookup"><span data-stu-id="ba3ae-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="ba3ae-104">Permite la extensión a contenido enriquecido para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba3ae-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ba3ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba3ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba3ae-107">*dwContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-108">Type: **DWORD**</span></span>

<span data-ttu-id="ba3ae-109">Identificador de contexto para la operación.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-109">The context identifier for the operation.</span></span> <span data-ttu-id="ba3ae-110">Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="ba3ae-111">*pwszProp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="ba3ae-113">Puntero a la propiedad del contenido vinculado como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="ba3ae-114">*Pinfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-115">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="ba3ae-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="ba3ae-116">Recibe un puntero a la estructura [_ *LINKINFO* \*](-search-linkinfo.md) en la que el método devuelve información sobre la transacción.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="ba3ae-117">*Pinfo* no debe ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ba3ae-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba3ae-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba3ae-118">Return value</span></span>

<span data-ttu-id="ba3ae-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-119">Type: **HRESULT**</span></span>

<span data-ttu-id="ba3ae-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba3ae-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba3ae-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba3ae-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba3ae-122">Remarks</span></span>

<span data-ttu-id="ba3ae-123">La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="ba3ae-124">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="ba3ae-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3ae-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba3ae-125">Requirements</span></span>



| <span data-ttu-id="ba3ae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba3ae-126">Requirement</span></span> | <span data-ttu-id="ba3ae-127">Value</span><span class="sxs-lookup"><span data-stu-id="ba3ae-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba3ae-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3ae-129">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ba3ae-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3ae-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ba3ae-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ba3ae-132">Redistributable</span></span><br/>          | <span data-ttu-id="ba3ae-133">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="ba3ae-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ba3ae-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba3ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3ae-135">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




