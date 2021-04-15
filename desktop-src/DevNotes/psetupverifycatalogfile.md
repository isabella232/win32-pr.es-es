---
description: Comprueba un solo archivo de catálogo mediante la Directiva de firma de código del sistema operativo estándar, como la firma de controladores.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649563"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="178dd-103">pSetupVerifyCatalogFile función)</span><span class="sxs-lookup"><span data-stu-id="178dd-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="178dd-104">\[Esta función ya no es compatible con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="178dd-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="178dd-105">Para un archivo INF (instalación de dispositivo), los desarrolladores deben usar **SetupVerifyInfFile**.</span><span class="sxs-lookup"><span data-stu-id="178dd-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="178dd-106">Para validar un catálogo no basado en INF, use **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="178dd-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="178dd-107">Comprueba un solo archivo de catálogo mediante la Directiva de firma de código del sistema operativo estándar, como la firma de controladores.</span><span class="sxs-lookup"><span data-stu-id="178dd-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="178dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="178dd-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="178dd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="178dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="178dd-110">*CatalogFullPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="178dd-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="178dd-111">Ruta de acceso completa del archivo de catálogo que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="178dd-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="178dd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="178dd-112">Return value</span></span>

<span data-ttu-id="178dd-113">Si la función se ejecuta correctamente, devuelve el **error \_ Success**; de lo contrario, devuelve el error de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="178dd-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="178dd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="178dd-114">Remarks</span></span>

<span data-ttu-id="178dd-115">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="178dd-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="178dd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="178dd-116">Requirements</span></span>



| <span data-ttu-id="178dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="178dd-117">Requirement</span></span> | <span data-ttu-id="178dd-118">Value</span><span class="sxs-lookup"><span data-stu-id="178dd-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="178dd-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="178dd-119">DLL</span></span><br/> | <dl> <span data-ttu-id="178dd-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="178dd-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178dd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="178dd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178dd-122">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="178dd-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="178dd-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="178dd-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
