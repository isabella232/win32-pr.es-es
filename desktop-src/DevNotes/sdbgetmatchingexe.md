---
description: Busca el archivo ejecutable especificado.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907191"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="e9ef3-103">SdbGetMatchingExe función)</span><span class="sxs-lookup"><span data-stu-id="e9ef3-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="e9ef3-104">Busca el archivo ejecutable especificado.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ef3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9ef3-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="e9ef3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9ef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ef3-107">*hSDB* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-108">Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ef3-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef3-109">*szPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-110">Ruta de acceso del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef3-111">*szModuleName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-112">Nombre del módulo.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef3-113">*pszEnvironment* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-114">Variables de entorno que se van a usar como contexto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef3-115">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-116">Este parámetro puede ser 0 o **SDBGMEF \_ omitir \_ entorno** (0x1).</span><span class="sxs-lookup"><span data-stu-id="e9ef3-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="e9ef3-117">*pQueryResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef3-118">Estructura [**SDBQUERYRESULT**](sdbqueryresult.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ef3-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="e9ef3-119">Si no se encuentra ninguna coincidencia, la estructura contiene **TAGREF \_ null**.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ef3-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9ef3-120">Return value</span></span>

<span data-ttu-id="e9ef3-121">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="e9ef3-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ef3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9ef3-122">Remarks</span></span>

<span data-ttu-id="e9ef3-123">Cuando haya terminado con el [**TAGREF**](tagref.md)devuelto, libere el uso de la función [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ef3-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ef3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ef3-124">Requirements</span></span>



| <span data-ttu-id="e9ef3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ef3-125">Requirement</span></span> | <span data-ttu-id="e9ef3-126">Value</span><span class="sxs-lookup"><span data-stu-id="e9ef3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ef3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9ef3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ef3-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e9ef3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9ef3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ef3-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ef3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9ef3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9ef3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ef3-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef3-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ef3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9ef3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ef3-134">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="e9ef3-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="e9ef3-135">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="e9ef3-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




