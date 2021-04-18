---
description: Inicializa el recurso compartido de IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660893"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="50cee-103">FInitIMEShare función)</span><span class="sxs-lookup"><span data-stu-id="50cee-103">FInitIMEShare function</span></span>

<span data-ttu-id="50cee-104">Inicializa el recurso compartido de IME.</span><span class="sxs-lookup"><span data-stu-id="50cee-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50cee-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="50cee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50cee-106">Parameters</span></span>

<span data-ttu-id="50cee-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="50cee-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50cee-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50cee-108">Return value</span></span>

<span data-ttu-id="50cee-109">La función devuelve **true** si se realiza correctamente o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="50cee-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cee-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50cee-110">Remarks</span></span>

<span data-ttu-id="50cee-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="50cee-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="50cee-112">Se debe llamar a esta función antes de llamar a cualquier otra función de recurso compartido de IME.</span><span class="sxs-lookup"><span data-stu-id="50cee-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50cee-113">Requirements</span></span>



| <span data-ttu-id="50cee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50cee-114">Requirement</span></span> | <span data-ttu-id="50cee-115">Value</span><span class="sxs-lookup"><span data-stu-id="50cee-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50cee-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50cee-116">DLL</span></span><br/> | <dl> <span data-ttu-id="50cee-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50cee-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cee-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="50cee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cee-119">**EndIMEShare**</span><span class="sxs-lookup"><span data-stu-id="50cee-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
