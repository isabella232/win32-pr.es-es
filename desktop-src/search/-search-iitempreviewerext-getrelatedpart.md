---
description: Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'IItemPreviewerExt:: GetRelatedPart (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715017"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="b28da-103">IItemPreviewerExt:: GetRelatedPart (método)</span><span class="sxs-lookup"><span data-stu-id="b28da-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="b28da-104">Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.</span><span class="sxs-lookup"><span data-stu-id="b28da-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b28da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b28da-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b28da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b28da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b28da-107">*dwContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b28da-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28da-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b28da-108">Type: **DWORD**</span></span>

<span data-ttu-id="b28da-109">Identificador de contexto para la operación.</span><span class="sxs-lookup"><span data-stu-id="b28da-109">The context identifier for the operation.</span></span> <span data-ttu-id="b28da-110">Invalide el valor predeterminado de **dwContext** para establecer el identificador de contexto en un valor de su elección.</span><span class="sxs-lookup"><span data-stu-id="b28da-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="b28da-111">*pwszProp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b28da-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28da-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="b28da-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="b28da-113">Puntero a la propiedad del contenido vinculado como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="b28da-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="b28da-114">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b28da-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28da-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b28da-115">Type: **DWORD**</span></span>

<span data-ttu-id="b28da-116">Valor entero largo sin signo que contiene el índice de base cero de la parte del cuerpo relacionada.</span><span class="sxs-lookup"><span data-stu-id="b28da-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="b28da-117">*Pinfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b28da-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b28da-118">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b28da-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="b28da-119">Recibe un puntero a la estructura [_ *LINKINFO* \*](-search-linkinfo.md) en la que el método devuelve información sobre la transacción.</span><span class="sxs-lookup"><span data-stu-id="b28da-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="b28da-120">*Pinfo* no debe ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b28da-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b28da-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b28da-121">Return value</span></span>

<span data-ttu-id="b28da-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b28da-122">Type: **HRESULT**</span></span>

<span data-ttu-id="b28da-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b28da-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b28da-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b28da-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b28da-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b28da-125">Remarks</span></span>

<span data-ttu-id="b28da-126">La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="b28da-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b28da-127">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="b28da-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b28da-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b28da-128">Requirements</span></span>



| <span data-ttu-id="b28da-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28da-129">Requirement</span></span> | <span data-ttu-id="b28da-130">Value</span><span class="sxs-lookup"><span data-stu-id="b28da-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b28da-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b28da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b28da-132">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b28da-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b28da-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b28da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b28da-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b28da-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b28da-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b28da-135">Redistributable</span></span><br/>          | <span data-ttu-id="b28da-136">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b28da-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b28da-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b28da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28da-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="b28da-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




