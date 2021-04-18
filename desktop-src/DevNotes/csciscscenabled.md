---
description: Determina si Archivos sin conexión está habilitado.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661045"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="4c8cd-103">CSCIsCSCEnabled función)</span><span class="sxs-lookup"><span data-stu-id="4c8cd-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="4c8cd-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="4c8cd-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="4c8cd-105">Determina si Archivos sin conexión está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8cd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c8cd-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="4c8cd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c8cd-107">Parameters</span></span>

<span data-ttu-id="4c8cd-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c8cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c8cd-109">Return value</span></span>

<span data-ttu-id="4c8cd-110">Esta función devuelve **true** si archivos sin conexión está habilitado y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c8cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c8cd-111">Remarks</span></span>

<span data-ttu-id="4c8cd-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4c8cd-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8cd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c8cd-113">Requirements</span></span>



| <span data-ttu-id="4c8cd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8cd-114">Requirement</span></span> | <span data-ttu-id="4c8cd-115">Value</span><span class="sxs-lookup"><span data-stu-id="4c8cd-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8cd-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c8cd-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4c8cd-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c8cd-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c8cd-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c8cd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8cd-119">**CSCQueryDatabaseStatus**</span><span class="sxs-lookup"><span data-stu-id="4c8cd-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
