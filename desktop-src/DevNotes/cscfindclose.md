---
description: Cierra un identificador de búsqueda.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661048"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="b8e10-103">CSCFindClose función)</span><span class="sxs-lookup"><span data-stu-id="b8e10-103">CSCFindClose function</span></span>

<span data-ttu-id="b8e10-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="b8e10-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="b8e10-105">Cierra un identificador de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b8e10-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8e10-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="b8e10-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8e10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e10-108">*hFind* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8e10-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e10-109">Identificador de búsqueda devuelto por la función [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="b8e10-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e10-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8e10-110">Return value</span></span>

<span data-ttu-id="b8e10-111">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b8e10-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e10-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8e10-112">Remarks</span></span>

<span data-ttu-id="b8e10-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b8e10-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e10-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8e10-114">Requirements</span></span>



| <span data-ttu-id="b8e10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e10-115">Requirement</span></span> | <span data-ttu-id="b8e10-116">Value</span><span class="sxs-lookup"><span data-stu-id="b8e10-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e10-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8e10-117">DLL</span></span><br/> | <dl> <span data-ttu-id="b8e10-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e10-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e10-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8e10-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e10-120">**CSCFindFirstFileW**</span><span class="sxs-lookup"><span data-stu-id="b8e10-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
