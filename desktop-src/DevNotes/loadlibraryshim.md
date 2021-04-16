---
description: Carga una versión especificada de un archivo DLL de biblioteca .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670415"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="315f5-103">LoadLibraryShim (función)</span><span class="sxs-lookup"><span data-stu-id="315f5-103">LoadLibraryShim function</span></span>

<span data-ttu-id="315f5-104">Carga una versión especificada de un archivo DLL de biblioteca .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="315f5-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="315f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="315f5-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="315f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="315f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315f5-107">*szDllName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="315f5-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315f5-108">Nombre del archivo DLL que se va a cargar desde el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="315f5-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="315f5-109">*szVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="315f5-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315f5-110">Versión de la DLL que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="315f5-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="315f5-111">Si *szVersion* es **null**, se carga la versión más reciente de la dll especificada.</span><span class="sxs-lookup"><span data-stu-id="315f5-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="315f5-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="315f5-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="315f5-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="315f5-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="315f5-114">*phModDll* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="315f5-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="315f5-115">Identificador del módulo.</span><span class="sxs-lookup"><span data-stu-id="315f5-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315f5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="315f5-116">Return value</span></span>

<span data-ttu-id="315f5-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="315f5-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="315f5-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="315f5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="315f5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="315f5-119">Remarks</span></span>

<span data-ttu-id="315f5-120">Esta función se usa para cargar los archivos dll de biblioteca que se incluyen en el paquete redistribuible de .NET Framework, no en los archivos dll generados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="315f5-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="315f5-121">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="315f5-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="315f5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315f5-122">Requirements</span></span>



| <span data-ttu-id="315f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="315f5-123">Requirement</span></span> | <span data-ttu-id="315f5-124">Value</span><span class="sxs-lookup"><span data-stu-id="315f5-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="315f5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="315f5-125">DLL</span></span><br/> | <dl> <span data-ttu-id="315f5-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315f5-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
