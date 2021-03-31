---
title: CleanupCredentialCache función)
description: Implementado por determinados proveedores de compatibilidad para seguridad (SSP) para vaciar la caché de credenciales de SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Función CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149917"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="f78e7-104">CleanupCredentialCache función)</span><span class="sxs-lookup"><span data-stu-id="f78e7-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="f78e7-105">Algunos proveedores de compatibilidad para seguridad (SSP) implementan la función **CleanupCredentialCache** para vaciar la caché de credenciales de SSP.</span><span class="sxs-lookup"><span data-stu-id="f78e7-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78e7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f78e7-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="f78e7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f78e7-107">Parameters</span></span>

<span data-ttu-id="f78e7-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f78e7-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f78e7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f78e7-109">Return value</span></span>

<span data-ttu-id="f78e7-110">**True** si la función se ejecuta correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78e7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f78e7-111">Remarks</span></span>

<span data-ttu-id="f78e7-112">La función **CleanupCredentialCache** se implementa mediante el siguiente SSP:</span><span class="sxs-lookup"><span data-stu-id="f78e7-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="f78e7-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="f78e7-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="f78e7-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="f78e7-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="f78e7-115">La implementación de **CleanupCredentialCache** por parte de estos SSP siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="f78e7-116">Antes de intentar obtener un identificador de módulo para exportar **CleanupCredentialCache**, la aplicación debe comprobar que el SSP que se ha cargado es uno de los SSP conocidos que implementan la función **CleanupCredentialCache** .</span><span class="sxs-lookup"><span data-stu-id="f78e7-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="f78e7-117">Para vaciar la memoria caché de credenciales de SSP, la aplicación debe obtener un identificador de módulo para el SSP mediante una llamada a la función [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="f78e7-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="f78e7-118">Después de obtener el módulo, la aplicación debe exportar la función **CleanupCredentialCache** implementada por el SSP llamando a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , pasando el módulo devuelto por **GetModuleHandle** y **CleanupCredentialCache** como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="f78e7-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="f78e7-119">Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain o los constructores y destructores de objetos globales.</span><span class="sxs-lookup"><span data-stu-id="f78e7-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="f78e7-120">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="f78e7-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="f78e7-121">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="f78e7-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f78e7-122">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f78e7-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f78e7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78e7-123">Requirements</span></span>



| <span data-ttu-id="f78e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78e7-124">Requirement</span></span> | <span data-ttu-id="f78e7-125">Value</span><span class="sxs-lookup"><span data-stu-id="f78e7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78e7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f78e7-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f78e7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="f78e7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f78e7-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f78e7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="f78e7-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f78e7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f78e7-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f78e7-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

