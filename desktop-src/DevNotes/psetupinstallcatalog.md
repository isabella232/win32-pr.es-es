---
description: Instala un archivo de catálogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649959"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="8d60b-103">pSetupInstallCatalog función)</span><span class="sxs-lookup"><span data-stu-id="8d60b-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="8d60b-104">\[Esta función ya no es compatible con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d60b-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="8d60b-105">Los desarrolladores deben usar **CryptCATAdminAddCatalog**.\]</span><span class="sxs-lookup"><span data-stu-id="8d60b-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="8d60b-106">Instala un archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="8d60b-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d60b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d60b-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="8d60b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d60b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d60b-109">*CatalogFullPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d60b-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d60b-110">Ruta de acceso completa del catálogo que se va a instalar en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8d60b-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d60b-111">*NewBaseName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d60b-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d60b-112">Nuevo nombre base que se utilizará cuando se copie el archivo de catálogo en el almacén de catálogos.</span><span class="sxs-lookup"><span data-stu-id="8d60b-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="8d60b-113">*NewCatalogFullPath* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8d60b-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d60b-114">Opcionalmente, recibe la ruta de acceso completa del archivo de catálogo en el almacén de catálogos.</span><span class="sxs-lookup"><span data-stu-id="8d60b-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="8d60b-115">Este búfer debe ser al menos **una \_ ruta de acceso máxima** de bytes (versión ANSI) o chars (versión Unicode).</span><span class="sxs-lookup"><span data-stu-id="8d60b-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d60b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d60b-116">Return value</span></span>

<span data-ttu-id="8d60b-117">Si la función se ejecuta correctamente, **no devuelve ningún \_ error**; de lo contrario, devuelve un código de error de Win32 que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="8d60b-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d60b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d60b-118">Remarks</span></span>

<span data-ttu-id="8d60b-119">El sistema copia el archivo en un directorio especial y, de forma opcional, se le cambia el nombre.</span><span class="sxs-lookup"><span data-stu-id="8d60b-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="8d60b-120">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8d60b-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d60b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d60b-121">Requirements</span></span>



| <span data-ttu-id="8d60b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d60b-122">Requirement</span></span> | <span data-ttu-id="8d60b-123">Value</span><span class="sxs-lookup"><span data-stu-id="8d60b-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d60b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d60b-124">DLL</span></span><br/> | <dl> <span data-ttu-id="8d60b-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d60b-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d60b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d60b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d60b-127">**CryptCATAdminAddCatalog**</span><span class="sxs-lookup"><span data-stu-id="8d60b-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
