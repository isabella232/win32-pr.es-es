---
title: ITSRemoteProgram3 ServerStartApp, método
description: Especifica que una aplicación se inicie en la sesión remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Método ServerStartApp Servicios de Escritorio remoto
- Método ServerStartApp Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto, método ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686171"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="f917b-106">ITSRemoteProgram3:: ServerStartApp (método)</span><span class="sxs-lookup"><span data-stu-id="f917b-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="f917b-107">Especifica que una aplicación se inicie en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="f917b-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f917b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f917b-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="f917b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f917b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f917b-110">*bstrAppUserModelId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917b-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f917b-111">*bstrArguments* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917b-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f917b-112">*vbExpandEnvVarInArgumentsOnServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917b-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="f917b-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f917b-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="f917b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f917b-114">Return value</span></span>

<span data-ttu-id="f917b-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f917b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f917b-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f917b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f917b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f917b-117">Requirements</span></span>



| <span data-ttu-id="f917b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f917b-118">Requirement</span></span> | <span data-ttu-id="f917b-119">Value</span><span class="sxs-lookup"><span data-stu-id="f917b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f917b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f917b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f917b-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f917b-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f917b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f917b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f917b-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f917b-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="f917b-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f917b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f917b-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f917b-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f917b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f917b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f917b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f917b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f917b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f917b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f917b-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="f917b-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





