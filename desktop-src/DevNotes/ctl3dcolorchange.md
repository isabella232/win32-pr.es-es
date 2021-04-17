---
description: Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660702"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="fdbc0-103">Ctl3dColorChange función)</span><span class="sxs-lookup"><span data-stu-id="fdbc0-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="fdbc0-104">Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbc0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdbc0-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="fdbc0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdbc0-106">Parameters</span></span>

<span data-ttu-id="fdbc0-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdbc0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdbc0-108">Return value</span></span>

<span data-ttu-id="fdbc0-109">Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdbc0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdbc0-110">Remarks</span></span>

<span data-ttu-id="fdbc0-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fdbc0-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="fdbc0-112">Se debe llamar a esta función en el procedimiento de ventana principal de la aplicación para el mensaje de **\_ SYSCOLORCHANGE de WM** , como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="fdbc0-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fdbc0-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="fdbc0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdbc0-114">Requirements</span></span>



| <span data-ttu-id="fdbc0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdbc0-115">Requirement</span></span> | <span data-ttu-id="fdbc0-116">Value</span><span class="sxs-lookup"><span data-stu-id="fdbc0-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbc0-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fdbc0-117">DLL</span></span><br/> | <dl> <span data-ttu-id="fdbc0-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdbc0-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
