---
title: ITsSbResourcePluginStoreEx ReleaseTargetLock, método
description: Libera un bloqueo en un destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Método ReleaseTargetLock Servicios de Escritorio remoto
- Método ReleaseTargetLock Servicios de Escritorio remoto, interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto, método ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150492"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="864d8-106">ITsSbResourcePluginStoreEx:: ReleaseTargetLock (método)</span><span class="sxs-lookup"><span data-stu-id="864d8-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="864d8-107">Libera un bloqueo en un destino.</span><span class="sxs-lookup"><span data-stu-id="864d8-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="864d8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="864d8-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="864d8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="864d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="864d8-110">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="864d8-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="864d8-111">Un puntero al contexto devuelto por el método [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .</span><span class="sxs-lookup"><span data-stu-id="864d8-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="864d8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="864d8-112">Return value</span></span>

<span data-ttu-id="864d8-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="864d8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="864d8-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="864d8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="864d8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="864d8-115">Remarks</span></span>

<span data-ttu-id="864d8-116">Este método solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="864d8-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="864d8-117">Este método está disponible en la interfaz [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="864d8-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="864d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="864d8-118">Requirements</span></span>



| <span data-ttu-id="864d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="864d8-119">Requirement</span></span> | <span data-ttu-id="864d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="864d8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="864d8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="864d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="864d8-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="864d8-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="864d8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="864d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="864d8-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="864d8-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="864d8-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="864d8-125">End of server support</span></span><br/>    | <span data-ttu-id="864d8-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="864d8-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="864d8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="864d8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="864d8-128"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="864d8-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="864d8-129">IID</span><span class="sxs-lookup"><span data-stu-id="864d8-129">IID</span></span><br/>                      | <span data-ttu-id="864d8-130">IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="864d8-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="864d8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="864d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="864d8-132">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="864d8-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





