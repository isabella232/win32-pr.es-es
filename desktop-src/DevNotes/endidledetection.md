---
description: Finaliza la supervisión de inactividad.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649857"
---
# <a name="endidledetection-function"></a><span data-ttu-id="b417d-103">EndIdleDetection función)</span><span class="sxs-lookup"><span data-stu-id="b417d-103">EndIdleDetection function</span></span>

<span data-ttu-id="b417d-104">\[Esta función no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b417d-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b417d-105">En su lugar, use la función **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="b417d-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="b417d-106">Finaliza la supervisión de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b417d-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="b417d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b417d-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b417d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b417d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b417d-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="b417d-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="b417d-110">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="b417d-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b417d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b417d-111">Return value</span></span>

<span data-ttu-id="b417d-112">Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b417d-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b417d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b417d-113">Remarks</span></span>

<span data-ttu-id="b417d-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b417d-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="b417d-115">Esta función no se exporta por nombre; Especifique el ordinal 4 al llamar a **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="b417d-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b417d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b417d-116">Requirements</span></span>



| <span data-ttu-id="b417d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b417d-117">Requirement</span></span> | <span data-ttu-id="b417d-118">Value</span><span class="sxs-lookup"><span data-stu-id="b417d-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b417d-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b417d-119">DLL</span></span><br/> | <dl> <span data-ttu-id="b417d-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b417d-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b417d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b417d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b417d-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="b417d-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
