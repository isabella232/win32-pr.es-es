---
description: Desactiva la subclase para el control especificado.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650079"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="f3853-103">Ctl3dUnsubclassCtl función)</span><span class="sxs-lookup"><span data-stu-id="f3853-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="f3853-104">Desactiva la subclase para el control especificado.</span><span class="sxs-lookup"><span data-stu-id="f3853-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3853-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3853-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="f3853-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3853-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="f3853-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f3853-108">Identificador de la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="f3853-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3853-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3853-109">Return value</span></span>

<span data-ttu-id="f3853-110">Devuelve **true** si el control se ha subclase correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f3853-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3853-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3853-111">Remarks</span></span>

<span data-ttu-id="f3853-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f3853-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3853-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3853-113">Requirements</span></span>



| <span data-ttu-id="f3853-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3853-114">Requirement</span></span> | <span data-ttu-id="f3853-115">Value</span><span class="sxs-lookup"><span data-stu-id="f3853-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3853-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3853-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f3853-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3853-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3853-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3853-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3853-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="f3853-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
