---
title: Método ResourceLocator. AddSelector (WSManDisp. h)
description: Agrega un selector al objeto ResourceLocator. El selector especifica una instancia concreta de un recurso.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Método AddSelector Administración remota de Windows
- Método AddSelector Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996440"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="af231-107">ResourceLocator. AddSelector, método</span><span class="sxs-lookup"><span data-stu-id="af231-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="af231-108">Agrega un [*selector*](windows-remote-management-glossary.md) al objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="af231-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="af231-109">El selector especifica una instancia concreta de un *recurso*.</span><span class="sxs-lookup"><span data-stu-id="af231-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="af231-110">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="af231-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="af231-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af231-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="af231-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af231-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af231-113">*resourceSelName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af231-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af231-114">Nombre del selector.</span><span class="sxs-lookup"><span data-stu-id="af231-114">The selector name.</span></span> <span data-ttu-id="af231-115">Por ejemplo, al solicitar datos WMI, este parámetro es la propiedad clave de una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="af231-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="af231-116">*selValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af231-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af231-117">Valor del selector.</span><span class="sxs-lookup"><span data-stu-id="af231-117">The selector value.</span></span> <span data-ttu-id="af231-118">Por ejemplo, para los datos de WMI, este parámetro contiene un valor para una propiedad de clave que identifica una instancia específica.</span><span class="sxs-lookup"><span data-stu-id="af231-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af231-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af231-119">Remarks</span></span>

<span data-ttu-id="af231-120">**IWSManResourceLocator:: AddSelector** es el método de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af231-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="af231-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af231-121">Requirements</span></span>



| <span data-ttu-id="af231-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="af231-122">Requirement</span></span> | <span data-ttu-id="af231-123">Value</span><span class="sxs-lookup"><span data-stu-id="af231-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af231-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af231-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af231-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af231-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="af231-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af231-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af231-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af231-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="af231-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af231-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af231-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af231-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af231-130">IDL</span><span class="sxs-lookup"><span data-stu-id="af231-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af231-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af231-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="af231-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af231-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="af231-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af231-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af231-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af231-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af231-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af231-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af231-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="af231-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af231-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="af231-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





