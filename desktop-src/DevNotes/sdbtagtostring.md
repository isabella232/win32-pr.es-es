---
description: Recupera el nombre para mostrar de la etiqueta especificada.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496096"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="21098-103">SdbTagToString función)</span><span class="sxs-lookup"><span data-stu-id="21098-103">SdbTagToString function</span></span>

<span data-ttu-id="21098-104">Recupera el nombre para mostrar de la etiqueta especificada.</span><span class="sxs-lookup"><span data-stu-id="21098-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="21098-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21098-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="21098-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21098-107">*etiqueta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="21098-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21098-108">ETIQUETA.</span><span class="sxs-lookup"><span data-stu-id="21098-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21098-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21098-109">Return value</span></span>

<span data-ttu-id="21098-110">La función devuelve un puntero a la cadena terminada en null o "InvalidTag".</span><span class="sxs-lookup"><span data-stu-id="21098-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="21098-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21098-111">Requirements</span></span>



| <span data-ttu-id="21098-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="21098-112">Requirement</span></span> | <span data-ttu-id="21098-113">Value</span><span class="sxs-lookup"><span data-stu-id="21098-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21098-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21098-114">Minimum supported client</span></span><br/> | <span data-ttu-id="21098-115">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="21098-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="21098-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21098-116">Minimum supported server</span></span><br/> | <span data-ttu-id="21098-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="21098-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="21098-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21098-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21098-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21098-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21098-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="21098-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21098-121">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="21098-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




