---
description: Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P método rocessTransformCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907752"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="dd96d-103">IItemPreviewerExt::P método rocessTransformCommand</span><span class="sxs-lookup"><span data-stu-id="dd96d-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="dd96d-104">Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.</span><span class="sxs-lookup"><span data-stu-id="dd96d-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd96d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd96d-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="dd96d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd96d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd96d-107">*dwContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96d-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="dd96d-108">Type: **DWORD**</span></span>

<span data-ttu-id="dd96d-109">Identificador de contexto para la operación.</span><span class="sxs-lookup"><span data-stu-id="dd96d-109">The context identifier for the operation.</span></span> <span data-ttu-id="dd96d-110">Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.</span><span class="sxs-lookup"><span data-stu-id="dd96d-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="dd96d-111">*pwszName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96d-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="dd96d-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="dd96d-113">Puntero al nombre del comando de transformación como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd96d-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="dd96d-114">*pwszArg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96d-115">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="dd96d-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="dd96d-116">Puntero al argumento como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd96d-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="dd96d-117">*pvarResult* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96d-118">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="dd96d-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="dd96d-119">Puntero a la variante de resultado.</span><span class="sxs-lookup"><span data-stu-id="dd96d-119">A pointer to the result variant.</span></span> <span data-ttu-id="dd96d-120">_pvarResult \* no debe ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="dd96d-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd96d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd96d-121">Return value</span></span>

<span data-ttu-id="dd96d-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd96d-122">Type: **HRESULT**</span></span>

<span data-ttu-id="dd96d-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="dd96d-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd96d-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd96d-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd96d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd96d-125">Remarks</span></span>

<span data-ttu-id="dd96d-126">La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="dd96d-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="dd96d-127">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="dd96d-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd96d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd96d-128">Requirements</span></span>



| <span data-ttu-id="dd96d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd96d-129">Requirement</span></span> | <span data-ttu-id="dd96d-130">Value</span><span class="sxs-lookup"><span data-stu-id="dd96d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd96d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd96d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dd96d-132">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd96d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd96d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dd96d-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd96d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd96d-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dd96d-135">Redistributable</span></span><br/>          | <span data-ttu-id="dd96d-136">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="dd96d-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dd96d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd96d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd96d-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="dd96d-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




