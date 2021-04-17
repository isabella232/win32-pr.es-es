---
description: El método SetAsSingleton del objeto SWbemObjectPath obliga a la ruta de acceso a una instancia singleton de WMI de una clase. Una clase singleton es una clase que nunca puede tener más de una instancia.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Método SWbemObjectPath. SetAsSingleton (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717029"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="2532e-104">SWbemObjectPath. SetAsSingleton, método</span><span class="sxs-lookup"><span data-stu-id="2532e-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="2532e-105">El método **SetAsSingleton** del objeto [**SWbemObjectPath**](swbemobjectpath.md) obliga a la ruta de acceso a una instancia singleton de WMI de una clase.</span><span class="sxs-lookup"><span data-stu-id="2532e-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="2532e-106">Una clase singleton es una clase que nunca puede tener más de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2532e-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="2532e-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2532e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="2532e-108">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="2532e-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="2532e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2532e-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="2532e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2532e-110">Parameters</span></span>

<span data-ttu-id="2532e-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2532e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2532e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2532e-112">Return value</span></span>

<span data-ttu-id="2532e-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2532e-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2532e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2532e-114">Error codes</span></span>

<span data-ttu-id="2532e-115">Al completarse el método **SetAsSingleton** , el objeto **Err** puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="2532e-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="2532e-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2532e-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2532e-117">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2532e-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2532e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2532e-118">Requirements</span></span>



| <span data-ttu-id="2532e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2532e-119">Requirement</span></span> | <span data-ttu-id="2532e-120">Value</span><span class="sxs-lookup"><span data-stu-id="2532e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2532e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2532e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2532e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2532e-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2532e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2532e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2532e-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2532e-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2532e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2532e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2532e-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2532e-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2532e-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2532e-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2532e-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2532e-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2532e-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2532e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2532e-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2532e-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2532e-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="2532e-131">CLSID</span></span><br/>                    | <span data-ttu-id="2532e-132">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="2532e-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="2532e-133">IID</span><span class="sxs-lookup"><span data-stu-id="2532e-133">IID</span></span><br/>                      | <span data-ttu-id="2532e-134">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="2532e-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




