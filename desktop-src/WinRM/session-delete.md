---
title: Método Session. Delete (WSManDisp. h)
description: Elimina el recurso especificado en el URI del recurso.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Eliminar método Administración remota de Windows
- Método Delete Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, método Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996123"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="5d6a3-106">Session. Delete (método)</span><span class="sxs-lookup"><span data-stu-id="5d6a3-106">Session.Delete method</span></span>

<span data-ttu-id="5d6a3-107">Elimina el recurso especificado en el URI del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6a3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d6a3-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5d6a3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d6a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6a3-110">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d6a3-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d6a3-111">URI del recurso que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="5d6a3-112">También puede usar un objeto [**ResourceLocator**](resourcelocator.md) para especificar el recurso.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5d6a3-113">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5d6a3-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d6a3-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-114">Reserved for future use.</span></span> <span data-ttu-id="5d6a3-115">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6a3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d6a3-116">Return value</span></span>

<span data-ttu-id="5d6a3-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d6a3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d6a3-118">Remarks</span></span>

<span data-ttu-id="5d6a3-119">La siguiente sintaxis se usa para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="5d6a3-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5d6a3-120">Examples</span></span>

<span data-ttu-id="5d6a3-121">En el siguiente ejemplo de código de VBScript se eliminan los agentes de escucha configurados para el transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="5d6a3-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="5d6a3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d6a3-122">Requirements</span></span>



| <span data-ttu-id="5d6a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d6a3-123">Requirement</span></span> | <span data-ttu-id="5d6a3-124">Value</span><span class="sxs-lookup"><span data-stu-id="5d6a3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6a3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d6a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6a3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d6a3-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5d6a3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d6a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6a3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d6a3-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5d6a3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d6a3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d6a3-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a3-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d6a3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="5d6a3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d6a3-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a3-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d6a3-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d6a3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d6a3-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a3-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d6a3-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d6a3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6a3-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a3-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d6a3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d6a3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6a3-138">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="5d6a3-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





