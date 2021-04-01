---
description: La función IsRemoteNPP indica si el BLOB especificado especifica un NPP remoto.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Función IsRemoteNPP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812692"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="7b15c-103">IsRemoteNPP función)</span><span class="sxs-lookup"><span data-stu-id="7b15c-103">IsRemoteNPP function</span></span>

<span data-ttu-id="7b15c-104">La función **IsRemoteNPP** indica si el BLOB especificado especifica un NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="7b15c-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b15c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b15c-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="7b15c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b15c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b15c-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b15c-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b15c-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b15c-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b15c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b15c-109">Return value</span></span>

<span data-ttu-id="7b15c-110">Si la función se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="7b15c-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b15c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b15c-111">Remarks</span></span>

<span data-ttu-id="7b15c-112">Utilice esta función para comprobar si existe una categoría remota.</span><span class="sxs-lookup"><span data-stu-id="7b15c-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="7b15c-113">Asegúrese de que los nombres de equipo remoto y local son diferentes.</span><span class="sxs-lookup"><span data-stu-id="7b15c-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b15c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b15c-114">Requirements</span></span>



| <span data-ttu-id="7b15c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b15c-115">Requirement</span></span> | <span data-ttu-id="7b15c-116">Value</span><span class="sxs-lookup"><span data-stu-id="7b15c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b15c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b15c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b15c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b15c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b15c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b15c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b15c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b15c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b15c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b15c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b15c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b15c-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="7b15c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b15c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b15c-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b15c-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b15c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b15c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b15c-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b15c-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




