---
description: Controla el \_ mensaje de CTLCOLOR de WM para las aplicaciones que usan CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650039"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="75323-103">Ctl3dCtlColorEx función)</span><span class="sxs-lookup"><span data-stu-id="75323-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="75323-104">Controla el mensaje de **\_ CTLCOLOR de WM** para las aplicaciones que usan CTL3D.</span><span class="sxs-lookup"><span data-stu-id="75323-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="75323-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75323-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="75323-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75323-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75323-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="75323-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="75323-108">Mensaje **de \_ CTLCOLOR de WM** para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75323-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="75323-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75323-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75323-110">Identificador del contexto de presentación (DC).</span><span class="sxs-lookup"><span data-stu-id="75323-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="75323-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75323-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75323-112">Identificador de una ventana secundaria (control).</span><span class="sxs-lookup"><span data-stu-id="75323-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75323-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75323-113">Return value</span></span>

<span data-ttu-id="75323-114">Devuelve un identificador al pincel adecuado si la función se ejecuta correctamente; de lo contrario, devuelve que `(HBRUSH)(0)` indica que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="75323-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="75323-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75323-115">Remarks</span></span>

<span data-ttu-id="75323-116">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="75323-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="75323-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75323-117">Requirements</span></span>



| <span data-ttu-id="75323-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75323-118">Requirement</span></span> | <span data-ttu-id="75323-119">Value</span><span class="sxs-lookup"><span data-stu-id="75323-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75323-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75323-120">DLL</span></span><br/> | <dl> <span data-ttu-id="75323-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75323-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
