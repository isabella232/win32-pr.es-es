---
title: Session.Batpropiedad chItems (WSManDisp. h)
description: Establece y obtiene el número de elementos de cada lote de enumeración.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad BatchItems
- Propiedad BatchItems Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, propiedad BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714614"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="7faa3-106">Session.Batpropiedad chItems</span><span class="sxs-lookup"><span data-stu-id="7faa3-106">Session.BatchItems property</span></span>

<span data-ttu-id="7faa3-107">Establece y obtiene el número de elementos de cada lote de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7faa3-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="7faa3-108">Este valor no se puede cambiar durante una enumeración.</span><span class="sxs-lookup"><span data-stu-id="7faa3-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="7faa3-109">El proveedor de recursos puede establecer un límite.</span><span class="sxs-lookup"><span data-stu-id="7faa3-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="7faa3-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7faa3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faa3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7faa3-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="7faa3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7faa3-112">Property value</span></span>

<span data-ttu-id="7faa3-113">Especifica el número máximo de elementos devueltos para cada llamada de red subyacente al servicio.</span><span class="sxs-lookup"><span data-stu-id="7faa3-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="7faa3-114">El valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="7faa3-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="7faa3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7faa3-115">Remarks</span></span>

<span data-ttu-id="7faa3-116">Se trata de una característica de optimización que controla la frecuencia con que se realizan las llamadas de red entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="7faa3-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="7faa3-117">Actualmente, solo se usa para las enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="7faa3-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="7faa3-118">Para obtener más información sobre la enumeración de recursos, vea [**enumerar**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="7faa3-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7faa3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7faa3-119">Requirements</span></span>



| <span data-ttu-id="7faa3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7faa3-120">Requirement</span></span> | <span data-ttu-id="7faa3-121">Value</span><span class="sxs-lookup"><span data-stu-id="7faa3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7faa3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7faa3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7faa3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7faa3-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7faa3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7faa3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7faa3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7faa3-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7faa3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7faa3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7faa3-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7faa3-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7faa3-128">IDL</span><span class="sxs-lookup"><span data-stu-id="7faa3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7faa3-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7faa3-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7faa3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7faa3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7faa3-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7faa3-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7faa3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7faa3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7faa3-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7faa3-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7faa3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7faa3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faa3-135">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="7faa3-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="7faa3-136">**Enumerar**</span><span class="sxs-lookup"><span data-stu-id="7faa3-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="7faa3-137">**Enumerador. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="7faa3-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





