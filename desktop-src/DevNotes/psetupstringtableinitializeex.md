---
description: Inicializa una tabla de cadenas.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx función)
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
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670512"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="7f31e-103">pSetupStringTableInitializeEx función)</span><span class="sxs-lookup"><span data-stu-id="7f31e-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="7f31e-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="7f31e-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="7f31e-105">Inicializa una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7f31e-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f31e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f31e-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="7f31e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f31e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f31e-108">*ExtraDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f31e-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f31e-109">Tamaño del objeto de datos extra.</span><span class="sxs-lookup"><span data-stu-id="7f31e-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="7f31e-110">*Reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f31e-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f31e-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7f31e-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f31e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f31e-112">Remarks</span></span>

<span data-ttu-id="7f31e-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7f31e-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f31e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f31e-114">Requirements</span></span>



| <span data-ttu-id="7f31e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f31e-115">Requirement</span></span> | <span data-ttu-id="7f31e-116">Value</span><span class="sxs-lookup"><span data-stu-id="7f31e-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f31e-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f31e-117">DLL</span></span><br/> | <dl> <span data-ttu-id="7f31e-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f31e-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
