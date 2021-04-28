---
description: 'Función pSetupStringTableInitialize: inicializa una tabla de cadenas.'
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: función pSetupStringTableInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089204"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="d1083-103">función pSetupStringTableInitialize</span><span class="sxs-lookup"><span data-stu-id="d1083-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="d1083-104">\[Esta función no está disponible en Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="d1083-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="d1083-105">Inicializa una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="d1083-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1083-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1083-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="d1083-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1083-107">Parameters</span></span>

<span data-ttu-id="d1083-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d1083-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1083-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1083-109">Remarks</span></span>

<span data-ttu-id="d1083-110">Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="d1083-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1083-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1083-111">Requirements</span></span>



| <span data-ttu-id="d1083-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1083-112">Requirement</span></span> | <span data-ttu-id="d1083-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d1083-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1083-114">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1083-114">DLL</span></span><br/> | <dl> <span data-ttu-id="d1083-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1083-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
