---
description: Obtiene información acerca de la versión del sistema operativo.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660298"
---
# <a name="_getversionex-function"></a><span data-ttu-id="e6bf0-103">\_GetVersionEx (función)</span><span class="sxs-lookup"><span data-stu-id="e6bf0-103">\_GetVersionEx function</span></span>

<span data-ttu-id="e6bf0-104">\[Esta función es un contenedor de la función **GetVersionEx** .</span><span class="sxs-lookup"><span data-stu-id="e6bf0-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="e6bf0-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="e6bf0-106">Las aplicaciones deben llamar a **GetVersionEx** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="e6bf0-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="e6bf0-107">Obtiene información acerca de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-107">Gets information about the operating system version.</span></span> <span data-ttu-id="e6bf0-108">Vea [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="e6bf0-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6bf0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6bf0-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="e6bf0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6bf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6bf0-111">*...*</span><span class="sxs-lookup"><span data-stu-id="e6bf0-111">*...*</span></span> 
<span data-ttu-id="e6bf0-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e6bf0-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e6bf0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6bf0-113">Requirements</span></span>



| <span data-ttu-id="e6bf0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6bf0-114">Requirement</span></span> | <span data-ttu-id="e6bf0-115">Value</span><span class="sxs-lookup"><span data-stu-id="e6bf0-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bf0-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6bf0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e6bf0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6bf0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6bf0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6bf0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6bf0-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="e6bf0-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
