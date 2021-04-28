---
description: 'Función pSetupStringTableInitializeEx: inicializa una tabla de cadenas.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Función pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096653"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="f88ef-103">Función pSetupStringTableInitializeEx</span><span class="sxs-lookup"><span data-stu-id="f88ef-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="f88ef-104">\[Esta función no está disponible en Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="f88ef-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="f88ef-105">Inicializa una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f88ef-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88ef-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f88ef-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="f88ef-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f88ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f88ef-108">*ExtraDataSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f88ef-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ef-109">Tamaño del objeto de datos adicional.</span><span class="sxs-lookup"><span data-stu-id="f88ef-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="f88ef-110">*Reservado* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f88ef-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ef-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f88ef-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f88ef-112">Remarks</span></span>

<span data-ttu-id="f88ef-113">Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="f88ef-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f88ef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f88ef-114">Requirements</span></span>



| <span data-ttu-id="f88ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f88ef-115">Requirement</span></span> | <span data-ttu-id="f88ef-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f88ef-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f88ef-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f88ef-117">DLL</span></span><br/> | <dl> <span data-ttu-id="f88ef-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f88ef-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
