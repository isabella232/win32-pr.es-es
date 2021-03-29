---
title: Método TestAndSetState de la clase Win32_RDSHServer
description: Compara el estado actual con el especificado. Si los dos coinciden, el estado se establece en un nuevo valor. Independientemente de la coincidencia, también se devuelve el estado actual.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Método TestAndSetState Servicios de Escritorio remoto
- Método TestAndSetState Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150387"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="c2ac9-107">Método TestAndSetState de la \_ clase RDSHServer de Win32</span><span class="sxs-lookup"><span data-stu-id="c2ac9-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="c2ac9-108">Compara el estado actual con el especificado. Si los dos coinciden, el estado se establece en un nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="c2ac9-109">Independientemente de la coincidencia, también se devuelve el estado actual.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ac9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2ac9-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="c2ac9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2ac9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ac9-112">*Comparand* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2ac9-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ac9-113">Valor que se va a comparar con el estado actual; Si los dos valores coinciden, el estado se establece en *NewState*.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="c2ac9-114">*NewState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2ac9-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ac9-115">Nuevo valor del estado.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="c2ac9-116">*InitState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c2ac9-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ac9-117">Si se realiza correctamente o con errores, devuelve el estado actual.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2ac9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2ac9-118">Requirements</span></span>



| <span data-ttu-id="c2ac9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2ac9-119">Requirement</span></span> | <span data-ttu-id="c2ac9-120">Value</span><span class="sxs-lookup"><span data-stu-id="c2ac9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ac9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2ac9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ac9-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c2ac9-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c2ac9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2ac9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ac9-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c2ac9-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="c2ac9-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2ac9-125">Namespace</span></span><br/>                | <span data-ttu-id="c2ac9-126">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c2ac9-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c2ac9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c2ac9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2ac9-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2ac9-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2ac9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2ac9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2ac9-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2ac9-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c2ac9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ac9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ac9-132">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





