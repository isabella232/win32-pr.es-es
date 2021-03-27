---
description: Inicializa o reinicializa la lista de imágenes del sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360682"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="8babe-103">FileIconInit función)</span><span class="sxs-lookup"><span data-stu-id="8babe-103">FileIconInit function</span></span>

<span data-ttu-id="8babe-104">Inicializa o reinicializa la lista de imágenes del sistema.</span><span class="sxs-lookup"><span data-stu-id="8babe-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8babe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8babe-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="8babe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8babe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8babe-107">*fRestoreCache* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8babe-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8babe-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8babe-108">Type: **BOOL**</span></span>

<span data-ttu-id="8babe-109">**True** para restaurar la memoria caché de la imagen del sistema desde el disco; De lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="8babe-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8babe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8babe-110">Return value</span></span>

<span data-ttu-id="8babe-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8babe-111">Type: **BOOL**</span></span>

<span data-ttu-id="8babe-112">**True** si la memoria caché se actualizó correctamente, **false** si se produjo un error en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8babe-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8babe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8babe-113">Remarks</span></span>

<span data-ttu-id="8babe-114">Si usa listas de imágenes del sistema en su propio proceso, debe llamar a **FileIconInit** en los momentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8babe-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="8babe-115">Al iniciar.</span><span class="sxs-lookup"><span data-stu-id="8babe-115">On launch.</span></span>
-   <span data-ttu-id="8babe-116">En respuesta a un mensaje de [**\_ SETTINGCHANGE de WM**](../winmsg/wm-settingchange.md) cuando se establece la marca [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8babe-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="8babe-117">**FileIconInit** no se incluye en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8babe-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="8babe-118">Debe llamarlo directamente desde Shell32.dll, utilizando el ordinal 660.</span><span class="sxs-lookup"><span data-stu-id="8babe-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="8babe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8babe-119">Requirements</span></span>



| <span data-ttu-id="8babe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8babe-120">Requirement</span></span> | <span data-ttu-id="8babe-121">Value</span><span class="sxs-lookup"><span data-stu-id="8babe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8babe-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8babe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8babe-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8babe-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8babe-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8babe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8babe-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8babe-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8babe-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8babe-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8babe-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8babe-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
