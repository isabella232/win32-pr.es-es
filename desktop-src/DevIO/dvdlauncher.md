---
description: Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153333"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="7444a-103">DvdLauncher función)</span><span class="sxs-lookup"><span data-stu-id="7444a-103">DvdLauncher function</span></span>

<span data-ttu-id="7444a-104">Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="7444a-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="7444a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7444a-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="7444a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7444a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7444a-107">*HWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7444a-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7444a-108">Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.</span><span class="sxs-lookup"><span data-stu-id="7444a-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="7444a-109">*LetraDeUnidad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7444a-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7444a-110">Letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="7444a-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7444a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7444a-111">Return value</span></span>

<span data-ttu-id="7444a-112">Si la función se ejecuta correctamente y las regiones coinciden, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="7444a-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="7444a-113">De lo contrario, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="7444a-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7444a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7444a-114">Remarks</span></span>

<span data-ttu-id="7444a-115">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="7444a-115">This function has no associated import library.</span></span> <span data-ttu-id="7444a-116">Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a StorProp.dll.</span><span class="sxs-lookup"><span data-stu-id="7444a-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7444a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7444a-117">Requirements</span></span>



| <span data-ttu-id="7444a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7444a-118">Requirement</span></span> | <span data-ttu-id="7444a-119">Value</span><span class="sxs-lookup"><span data-stu-id="7444a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7444a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7444a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7444a-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7444a-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7444a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7444a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7444a-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7444a-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7444a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7444a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7444a-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7444a-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7444a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7444a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7444a-127">Funciones de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="7444a-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

