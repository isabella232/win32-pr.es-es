---
description: Determina si la Terminal Server está en el modo de instalación.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649532"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="7b814-103">TermsrvAppInstallMode función)</span><span class="sxs-lookup"><span data-stu-id="7b814-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="7b814-104">\[Esta función no se admite y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="7b814-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="7b814-105">Puede cambiar o desaparecer por completo sin aviso previo.\]</span><span class="sxs-lookup"><span data-stu-id="7b814-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="7b814-106">Determina si la Terminal Server está en el modo de instalación.</span><span class="sxs-lookup"><span data-stu-id="7b814-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b814-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b814-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="7b814-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b814-108">Parameters</span></span>

<span data-ttu-id="7b814-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b814-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b814-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b814-110">Return value</span></span>

<span data-ttu-id="7b814-111">Esta función devuelve **true** si el Terminal Server está en modo de instalación y **false** si está en modo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7b814-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b814-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b814-112">Requirements</span></span>



| <span data-ttu-id="7b814-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b814-113">Requirement</span></span> | <span data-ttu-id="7b814-114">Value</span><span class="sxs-lookup"><span data-stu-id="7b814-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b814-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b814-115">DLL</span></span><br/> | <dl> <span data-ttu-id="7b814-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b814-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




