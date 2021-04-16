---
description: Determina si el Terminal Server está en modo de instalación (solo en Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650077"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="3745b-103">CtxGetIniMapping función)</span><span class="sxs-lookup"><span data-stu-id="3745b-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="3745b-104">\[Esta función no se admite y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3745b-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="3745b-105">Puede cambiar o desaparecer por completo sin aviso previo.</span><span class="sxs-lookup"><span data-stu-id="3745b-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="3745b-106">En su lugar, use **VerifyVersionInfo**.\]</span><span class="sxs-lookup"><span data-stu-id="3745b-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="3745b-107">Determina si el Terminal Server está en modo de instalación (solo en Windows Terminal Server 4,0).</span><span class="sxs-lookup"><span data-stu-id="3745b-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="3745b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3745b-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="3745b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3745b-109">Parameters</span></span>

<span data-ttu-id="3745b-110">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3745b-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3745b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3745b-111">Return value</span></span>

<span data-ttu-id="3745b-112">Esta función devuelve **false** si el Terminal Server está en modo de instalación, es **true** si está en modo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3745b-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="3745b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3745b-113">Requirements</span></span>



| <span data-ttu-id="3745b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3745b-114">Requirement</span></span> | <span data-ttu-id="3745b-115">Value</span><span class="sxs-lookup"><span data-stu-id="3745b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3745b-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3745b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3745b-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3745b-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3745b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3745b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3745b-119">**VerifyVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="3745b-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
