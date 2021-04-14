---
description: Sugiere la Directiva de seguridad que se va a aplicar al explorador.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'IItemPreviewerExt:: SuggestBrowserPolicy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497074"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="6ffa2-103">IItemPreviewerExt:: SuggestBrowserPolicy (método)</span><span class="sxs-lookup"><span data-stu-id="6ffa2-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="6ffa2-104">Sugiere la Directiva de seguridad que se va a aplicar al explorador.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ffa2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ffa2-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6ffa2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ffa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ffa2-107">*dwContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ffa2-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ffa2-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6ffa2-108">Type: **DWORD**</span></span>

<span data-ttu-id="6ffa2-109">Identificador de contexto para la operación.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-109">The context identifier for the operation.</span></span> <span data-ttu-id="6ffa2-110">Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="6ffa2-111">*pdwFlags* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6ffa2-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6ffa2-112">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="6ffa2-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="6ffa2-113">Un puntero a un valor DWORD que contiene marcas de comprobación de comprobación.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="6ffa2-114">La marca _ *BROWSERPOLICY de \_ \_ contenido* que no es de confianza \* deshabilita cualquier posibilidad de que la vista previa pueda ejecutar script o ActiveX.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="6ffa2-115">El parámetro *pdwFlags* no debe ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6ffa2-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ffa2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ffa2-116">Return value</span></span>

<span data-ttu-id="6ffa2-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ffa2-117">Type: **HRESULT**</span></span>

<span data-ttu-id="6ffa2-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ffa2-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ffa2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ffa2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ffa2-120">Remarks</span></span>

<span data-ttu-id="6ffa2-121">La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="6ffa2-122">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffa2-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="6ffa2-123">Se recomienda encarecidamente usar la marca de **\_ \_ contenido** que no es de confianza de BROWSERPOLICY para deshabilitar la posibilidad de que la vista previa pueda ejecutar script o ActiveX.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="6ffa2-124">El método **IItemPreviewerExt:: SuggestBrowserPolicy** puede devolver información sobre si el elemento que se está previsualizando es de confianza o no.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="6ffa2-125">Esto permitirá que el control Trident del controlador de vista previa ejecute un script e incluso controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="6ffa2-126">Dado que el previsor suele usar archivos temporales para generar la vista previa, al hacerlo se puede producir un script y una ejecución de código inesperados en la zona de equipo local.</span><span class="sxs-lookup"><span data-stu-id="6ffa2-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffa2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ffa2-127">Requirements</span></span>



| <span data-ttu-id="6ffa2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ffa2-128">Requirement</span></span> | <span data-ttu-id="6ffa2-129">Value</span><span class="sxs-lookup"><span data-stu-id="6ffa2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ffa2-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ffa2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6ffa2-131">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ffa2-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6ffa2-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ffa2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6ffa2-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ffa2-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6ffa2-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6ffa2-134">Redistributable</span></span><br/>          | <span data-ttu-id="6ffa2-135">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="6ffa2-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6ffa2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ffa2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffa2-137">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="6ffa2-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




