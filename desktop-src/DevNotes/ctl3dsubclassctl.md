---
description: Subclases de un control individual a menos que el control aparezca en un cuadro de diálogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650056"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="84f1a-103">Ctl3dSubclassCtl función)</span><span class="sxs-lookup"><span data-stu-id="84f1a-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="84f1a-104">Subclases de un control individual a menos que el control aparezca en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="84f1a-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84f1a-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="84f1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f1a-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="84f1a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="84f1a-108">Identificador de la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="84f1a-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f1a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84f1a-109">Return value</span></span>

<span data-ttu-id="84f1a-110">Devuelve **true** si el control se ha subclase correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="84f1a-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f1a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84f1a-111">Remarks</span></span>

<span data-ttu-id="84f1a-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="84f1a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f1a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f1a-113">Requirements</span></span>



| <span data-ttu-id="84f1a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f1a-114">Requirement</span></span> | <span data-ttu-id="84f1a-115">Value</span><span class="sxs-lookup"><span data-stu-id="84f1a-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84f1a-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84f1a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="84f1a-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f1a-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f1a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="84f1a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f1a-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="84f1a-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
