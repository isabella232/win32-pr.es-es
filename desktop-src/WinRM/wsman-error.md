---
title: Propiedad WSMan. error (WSManDisp. h)
description: Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método WSMan si Administración remota de Windows servicio no pudo crear un objeto de sesión, un objeto ConnectionOptions o un objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Error de la propiedad Administración remota de Windows
- Propiedad error Administración remota de Windows, objeto WSMan
- Administración remota de Windows de objeto WSMan, propiedad error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150327"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="aa9c3-106">WSMan. error (propiedad)</span><span class="sxs-lookup"><span data-stu-id="aa9c3-106">WSMan.Error property</span></span>

<span data-ttu-id="aa9c3-107">Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método [**WSMan**](wsman.md) si administración remota de Windows servicio no pudo crear un objeto de [**sesión**](session.md) , un objeto [**ConnectionOptions**](connectionoptions.md) o un objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c3-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="aa9c3-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9c3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa9c3-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="aa9c3-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="aa9c3-110">Property value</span></span>

<span data-ttu-id="aa9c3-111">Representación XML de la información de error.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9c3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa9c3-112">Requirements</span></span>



| <span data-ttu-id="aa9c3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa9c3-113">Requirement</span></span> | <span data-ttu-id="aa9c3-114">Value</span><span class="sxs-lookup"><span data-stu-id="aa9c3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9c3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa9c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9c3-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa9c3-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="aa9c3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa9c3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9c3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9c3-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aa9c3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa9c3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9c3-120"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c3-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa9c3-121">IDL</span><span class="sxs-lookup"><span data-stu-id="aa9c3-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa9c3-122"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c3-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa9c3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa9c3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa9c3-124"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c3-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa9c3-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa9c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9c3-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c3-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa9c3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa9c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9c3-128">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="aa9c3-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





