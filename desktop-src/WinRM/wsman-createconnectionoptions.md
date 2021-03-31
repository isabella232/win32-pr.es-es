---
title: Método WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crea un objeto ConnectionOptions que especifica el nombre de usuario y la contraseña que se usan al crear una sesión.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Método CreateConnectionOptions Administración remota de Windows
- Administración remota de Windows método CreateConnectionOptions, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905114"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="d8c31-106">WSMan. CreateConnectionOptions (método)</span><span class="sxs-lookup"><span data-stu-id="d8c31-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="d8c31-107">Crea un objeto [**ConnectionOptions**](connectionoptions.md) que especifica el nombre de usuario y la contraseña que se usan al crear una sesión.</span><span class="sxs-lookup"><span data-stu-id="d8c31-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c31-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8c31-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="d8c31-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8c31-109">Parameters</span></span>

<span data-ttu-id="d8c31-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8c31-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8c31-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8c31-111">Return value</span></span>

<span data-ttu-id="d8c31-112">Un objeto [**ConnectionOptions**](connectionoptions.md) que se usa para especificar un par de nombre de usuario y contraseña que se usa para identificar un usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d8c31-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c31-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8c31-113">Remarks</span></span>

<span data-ttu-id="d8c31-114">La siguiente sintaxis se usa para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="d8c31-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="d8c31-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8c31-115">Requirements</span></span>



| <span data-ttu-id="d8c31-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c31-116">Requirement</span></span> | <span data-ttu-id="d8c31-117">Value</span><span class="sxs-lookup"><span data-stu-id="d8c31-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c31-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8c31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c31-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8c31-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d8c31-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8c31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c31-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8c31-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d8c31-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8c31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8c31-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8c31-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8c31-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d8c31-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8c31-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8c31-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8c31-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8c31-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8c31-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8c31-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8c31-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8c31-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8c31-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8c31-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8c31-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8c31-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c31-131">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="d8c31-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="d8c31-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="d8c31-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





