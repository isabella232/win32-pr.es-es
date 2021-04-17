---
description: Inicializa una tabla de cadenas.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize función)
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
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670515"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="4e40d-103">pSetupStringTableInitialize función)</span><span class="sxs-lookup"><span data-stu-id="4e40d-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="4e40d-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="4e40d-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="4e40d-105">Inicializa una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="4e40d-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e40d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e40d-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="4e40d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e40d-107">Parameters</span></span>

<span data-ttu-id="4e40d-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4e40d-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e40d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e40d-109">Remarks</span></span>

<span data-ttu-id="4e40d-110">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4e40d-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e40d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e40d-111">Requirements</span></span>



| <span data-ttu-id="4e40d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e40d-112">Requirement</span></span> | <span data-ttu-id="4e40d-113">Value</span><span class="sxs-lookup"><span data-stu-id="4e40d-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e40d-114">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e40d-114">DLL</span></span><br/> | <dl> <span data-ttu-id="4e40d-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e40d-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
