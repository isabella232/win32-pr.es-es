---
description: Esta función habilita o deshabilita la compatibilidad con los caracteres definidos por el usuario final (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984975"
---
# <a name="enableeudc-function"></a><span data-ttu-id="ee20c-103">EnableEUDC función)</span><span class="sxs-lookup"><span data-stu-id="ee20c-103">EnableEUDC function</span></span>

<span data-ttu-id="ee20c-104">Esta función habilita o deshabilita la compatibilidad con los caracteres definidos por el usuario final (EUDC).</span><span class="sxs-lookup"><span data-stu-id="ee20c-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee20c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee20c-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="ee20c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee20c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee20c-107">*fEnableEUDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee20c-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee20c-108">Valor booleano que se establece en **true** para habilitar EUDC y en **false** para deshabilitar EUDC.</span><span class="sxs-lookup"><span data-stu-id="ee20c-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee20c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee20c-109">Return value</span></span>

<span data-ttu-id="ee20c-110">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ee20c-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="ee20c-111">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ee20c-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee20c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee20c-112">Remarks</span></span>

<span data-ttu-id="ee20c-113">Si se deshabilita EUDC, si se intentan mostrar los caracteres de EUDC, se producirán glifos que faltan o que son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="ee20c-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="ee20c-114">Durante la sesión múltiple, esta función solo afecta a la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="ee20c-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="ee20c-115">Se recomienda usar esta función con Windows XP SP2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ee20c-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee20c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee20c-116">Requirements</span></span>



| <span data-ttu-id="ee20c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee20c-117">Requirement</span></span> | <span data-ttu-id="ee20c-118">Value</span><span class="sxs-lookup"><span data-stu-id="ee20c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee20c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee20c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee20c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ee20c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ee20c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee20c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee20c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee20c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee20c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee20c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee20c-124"><dt>Gdi32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee20c-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee20c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee20c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee20c-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee20c-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




