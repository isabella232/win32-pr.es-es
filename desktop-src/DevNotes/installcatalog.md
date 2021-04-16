---
description: Instala un catálogo en un directorio.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671398"
---
# <a name="installcatalog-function"></a><span data-ttu-id="0f043-103">InstallCatalog función)</span><span class="sxs-lookup"><span data-stu-id="0f043-103">InstallCatalog function</span></span>

<span data-ttu-id="0f043-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="0f043-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="0f043-105">Instala un catálogo en un directorio.</span><span class="sxs-lookup"><span data-stu-id="0f043-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f043-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f043-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="0f043-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f043-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f043-108">*CatalogFullPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f043-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f043-109">Puntero a una cadena que representa la ruta de acceso completa del catálogo antes de la instalación.</span><span class="sxs-lookup"><span data-stu-id="0f043-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="0f043-110">*NewBaseName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f043-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f043-111">Puntero al nuevo nombre base.</span><span class="sxs-lookup"><span data-stu-id="0f043-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="0f043-112">*NewCatalogFullPath* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f043-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f043-113">Puntero a una cadena que representa la ruta de acceso completa del catálogo después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="0f043-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f043-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f043-114">Return value</span></span>

<span data-ttu-id="0f043-115">Esta función no está implementada actualmente, por lo que no devuelve un valor real.</span><span class="sxs-lookup"><span data-stu-id="0f043-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f043-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f043-116">Remarks</span></span>

<span data-ttu-id="0f043-117">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0f043-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f043-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f043-118">Requirements</span></span>



| <span data-ttu-id="0f043-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f043-119">Requirement</span></span> | <span data-ttu-id="0f043-120">Value</span><span class="sxs-lookup"><span data-stu-id="0f043-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f043-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f043-121">DLL</span></span><br/> | <dl> <span data-ttu-id="0f043-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f043-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
