---
description: La función ExpertGetStartupInfo recupera la información de configuración de inicio del experto.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Función ExpertGetStartupInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423683"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="157b7-103">ExpertGetStartupInfo función)</span><span class="sxs-lookup"><span data-stu-id="157b7-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="157b7-104">La función **ExpertGetStartupInfo** recupera la información de configuración de inicio del experto.</span><span class="sxs-lookup"><span data-stu-id="157b7-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="157b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="157b7-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="157b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="157b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="157b7-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="157b7-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="157b7-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="157b7-108">Unique expert identifier.</span></span> <span data-ttu-id="157b7-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="157b7-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="157b7-110">*pExpertStartupInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="157b7-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="157b7-111">Puntero a una estructura [EXPERTSTARTUPINFO](expertstartupinfo.md) que contiene información de inicio.</span><span class="sxs-lookup"><span data-stu-id="157b7-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="157b7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="157b7-112">Return value</span></span>

<span data-ttu-id="157b7-113">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="157b7-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="157b7-114">Si la función no es correcta, el valor devuelto es NMERR.</span><span class="sxs-lookup"><span data-stu-id="157b7-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="157b7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="157b7-115">Remarks</span></span>

<span data-ttu-id="157b7-116">La función **ExpertGetStartupInfo** se utiliza si el experto debe determinar la información de inicio que se usa.</span><span class="sxs-lookup"><span data-stu-id="157b7-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="157b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="157b7-117">Requirements</span></span>



| <span data-ttu-id="157b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="157b7-118">Requirement</span></span> | <span data-ttu-id="157b7-119">Value</span><span class="sxs-lookup"><span data-stu-id="157b7-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="157b7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="157b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="157b7-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="157b7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="157b7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="157b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="157b7-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="157b7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="157b7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="157b7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="157b7-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="157b7-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="157b7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="157b7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="157b7-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="157b7-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="157b7-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="157b7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="157b7-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="157b7-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




