---
description: Recupera el directorio AppPatch del sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152707"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="bb023-103">SdbGetAppPatchDir función)</span><span class="sxs-lookup"><span data-stu-id="bb023-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="bb023-104">Recupera el directorio AppPatch del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb023-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb023-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb023-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="bb023-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb023-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb023-107">*hSDB* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bb023-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bb023-108">Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="bb023-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bb023-109">*szAppPatchPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb023-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb023-110">La ruta de acceso resultante.</span><span class="sxs-lookup"><span data-stu-id="bb023-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="bb023-111">*cchSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb023-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb023-112">Tamaño del búfer de *szAppPatchPath* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb023-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="bb023-113">Si se produce un error en la función, este parámetro se establece en la cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="bb023-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb023-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb023-114">Return value</span></span>

<span data-ttu-id="bb023-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bb023-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb023-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb023-116">Requirements</span></span>



| <span data-ttu-id="bb023-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb023-117">Requirement</span></span> | <span data-ttu-id="bb023-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb023-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb023-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb023-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb023-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb023-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bb023-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb023-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb023-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb023-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bb023-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb023-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb023-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb023-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb023-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb023-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb023-126">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="bb023-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




