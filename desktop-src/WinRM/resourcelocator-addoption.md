---
title: Método ResourceLocator. AddOption (WSManDisp. h)
description: Agrega datos adicionales necesarios para procesar la solicitud. Por ejemplo, algunos proveedores de WMI pueden requerir un objeto IWbemContext o SWbemNamedValueSet con información específica del proveedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Administración remota de Windows
- Método AddOption Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079021"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="211c6-107">ResourceLocator. AddOption, método</span><span class="sxs-lookup"><span data-stu-id="211c6-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="211c6-108">Agrega datos adicionales necesarios para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="211c6-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="211c6-109">Por ejemplo, algunos proveedores de WMI pueden requerir un objeto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con información específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="211c6-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="211c6-110">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="211c6-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="211c6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="211c6-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="211c6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="211c6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211c6-113">*OptionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="211c6-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211c6-114">Nombre (clave) del objeto de datos opcional.</span><span class="sxs-lookup"><span data-stu-id="211c6-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="211c6-115">*OptionValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="211c6-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211c6-116">Valor proporcionado para el objeto de datos opcional.</span><span class="sxs-lookup"><span data-stu-id="211c6-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="211c6-117">*mustComply* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="211c6-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211c6-118">Marca que indica que la opción se debe procesar.</span><span class="sxs-lookup"><span data-stu-id="211c6-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="211c6-119">El valor predeterminado es **false** (0).</span><span class="sxs-lookup"><span data-stu-id="211c6-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211c6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="211c6-120">Return value</span></span>

<span data-ttu-id="211c6-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="211c6-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="211c6-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="211c6-122">Remarks</span></span>

<span data-ttu-id="211c6-123">**IWSManResourceLocator:: AddOption** es el método de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="211c6-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="211c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="211c6-124">Requirements</span></span>



| <span data-ttu-id="211c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="211c6-125">Requirement</span></span> | <span data-ttu-id="211c6-126">Value</span><span class="sxs-lookup"><span data-stu-id="211c6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="211c6-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="211c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="211c6-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="211c6-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="211c6-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="211c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="211c6-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="211c6-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="211c6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="211c6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="211c6-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="211c6-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="211c6-133">IDL</span><span class="sxs-lookup"><span data-stu-id="211c6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="211c6-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="211c6-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="211c6-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="211c6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="211c6-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="211c6-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="211c6-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="211c6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211c6-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211c6-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="211c6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="211c6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211c6-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="211c6-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

