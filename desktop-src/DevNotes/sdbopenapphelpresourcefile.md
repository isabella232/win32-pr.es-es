---
description: Carga el archivo de recursos de apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423344"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="03b95-103">SdbOpenApphelpResourceFile función)</span><span class="sxs-lookup"><span data-stu-id="03b95-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="03b95-104">Carga el archivo de recursos de apphelp.</span><span class="sxs-lookup"><span data-stu-id="03b95-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03b95-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="03b95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03b95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03b95-107">*pwszACResourceFile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="03b95-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03b95-108">Ruta de acceso al archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03b95-108">The path to the resource file.</span></span> <span data-ttu-id="03b95-109">Si este parámetro es **null**, se abre el archivo dll de recursos local.</span><span class="sxs-lookup"><span data-stu-id="03b95-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03b95-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03b95-110">Return value</span></span>

<span data-ttu-id="03b95-111">La función devuelve un identificador al archivo de recursos abierto.</span><span class="sxs-lookup"><span data-stu-id="03b95-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b95-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03b95-112">Requirements</span></span>



| <span data-ttu-id="03b95-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b95-113">Requirement</span></span> | <span data-ttu-id="03b95-114">Value</span><span class="sxs-lookup"><span data-stu-id="03b95-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03b95-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03b95-115">Minimum supported client</span></span><br/> | <span data-ttu-id="03b95-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="03b95-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03b95-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03b95-117">Minimum supported server</span></span><br/> | <span data-ttu-id="03b95-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="03b95-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03b95-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03b95-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b95-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b95-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




