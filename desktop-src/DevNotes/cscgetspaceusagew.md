---
description: Recupera información sobre el espacio utilizado por la memoria caché de Archivos sin conexión.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650009"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="1f490-103">CSCGetSpaceUsageW función)</span><span class="sxs-lookup"><span data-stu-id="1f490-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="1f490-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="1f490-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="1f490-105">Recupera información sobre el espacio utilizado por la memoria caché de Archivos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1f490-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f490-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f490-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="1f490-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f490-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f490-108">*lptzLocation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-109">Ubicación del directorio de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-110">*dwSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f490-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-111">Tamaño del búfer de *lptzLocation* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="1f490-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-112">*lpdwMaxSpaceHigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-113">**Valor DWORD** de orden superior del número máximo de bytes disponibles en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-114">*lpdwMaxSpaceLow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-115">**Valor DWORD** de orden inferior del número máximo de bytes disponibles en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-116">*lpdwCurrentSpaceHigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-117">**Valor DWORD** de orden superior del número actual de bytes disponibles en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-118">*lpdwCurrentSpaceLow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-119">**Valor DWORD** de orden inferior del número actual de bytes disponibles en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-120">*lpcntTotalFiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-121">Número total de archivos en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="1f490-122">*lpcntTotalDirs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f490-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f490-123">El número total de directorios en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1f490-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f490-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f490-124">Return value</span></span>

<span data-ttu-id="1f490-125">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1f490-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f490-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f490-126">Remarks</span></span>

<span data-ttu-id="1f490-127">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1f490-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f490-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f490-128">Requirements</span></span>



| <span data-ttu-id="1f490-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f490-129">Requirement</span></span> | <span data-ttu-id="1f490-130">Value</span><span class="sxs-lookup"><span data-stu-id="1f490-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f490-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f490-131">DLL</span></span><br/> | <dl> <span data-ttu-id="1f490-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f490-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
