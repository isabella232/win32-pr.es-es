---
description: Comprueba un solo archivo de catálogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649499"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="7ce18-103">VerifyCatalogFile función)</span><span class="sxs-lookup"><span data-stu-id="7ce18-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="7ce18-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="7ce18-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="7ce18-105">Comprueba un solo archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="7ce18-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce18-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ce18-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="7ce18-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ce18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce18-108">*CatalogFullPath*</span><span class="sxs-lookup"><span data-stu-id="7ce18-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7ce18-109">Ruta de acceso completa del archivo de catálogo que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="7ce18-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce18-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ce18-110">Return value</span></span>

<span data-ttu-id="7ce18-111">Si la función se ejecuta correctamente, devuelve el **error \_ Success**; de lo contrario, devuelve el error de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="7ce18-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="7ce18-112">Si el catálogo es un catálogo firmado con Authenticode, esta función devuelve un **error de \_ \_ \_ Editor de confianza Authenticode** si se realiza correctamente; de lo contrario, devuelve el **error no se \_ \_ \_ ha \_ establecido la confianza Authenticode**.</span><span class="sxs-lookup"><span data-stu-id="7ce18-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="7ce18-113">Si la función no puede determinar si el publicador es de confianza, también puede devolver un error no **\_ identificado \_**.</span><span class="sxs-lookup"><span data-stu-id="7ce18-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ce18-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ce18-114">Remarks</span></span>

<span data-ttu-id="7ce18-115">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7ce18-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce18-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce18-116">Requirements</span></span>



| <span data-ttu-id="7ce18-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce18-117">Requirement</span></span> | <span data-ttu-id="7ce18-118">Value</span><span class="sxs-lookup"><span data-stu-id="7ce18-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce18-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ce18-119">DLL</span></span><br/> | <dl> <span data-ttu-id="7ce18-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce18-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
