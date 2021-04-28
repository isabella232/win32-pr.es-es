---
description: 'Método reset de la Msvm_Keyboard clase : restablece el teclado virtual.'
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Método reset de la Msvm_Keyboard clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 14c3166ce57fab4693dec87d3d81a55f1f688aa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111713"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="875c4-103">Método Reset de la clase Keyboard de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="875c4-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="875c4-104">Restablece el teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="875c4-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="875c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="875c4-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="875c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="875c4-106">Parameters</span></span>

<span data-ttu-id="875c4-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="875c4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="875c4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="875c4-108">Return value</span></span>

<span data-ttu-id="875c4-109">Un valor devuelto de cero indica que el resultado es correcto.</span><span class="sxs-lookup"><span data-stu-id="875c4-109">A return value of zero indicates success.</span></span> <span data-ttu-id="875c4-110">Un valor devuelto de uno indica un error porque no se admite el método .</span><span class="sxs-lookup"><span data-stu-id="875c4-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="875c4-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="875c4-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="875c4-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="875c4-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="875c4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="875c4-113">Requirements</span></span>



| <span data-ttu-id="875c4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="875c4-114">Requirement</span></span> | <span data-ttu-id="875c4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="875c4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875c4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="875c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="875c4-117">Windows 8.1 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="875c4-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="875c4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="875c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="875c4-119">Solo aplicaciones de escritorio de Windows Server 2012 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="875c4-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="875c4-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="875c4-120">Namespace</span></span><br/>                | <span data-ttu-id="875c4-121">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="875c4-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="875c4-122">MOF</span><span class="sxs-lookup"><span data-stu-id="875c4-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="875c4-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="875c4-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="875c4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="875c4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875c4-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="875c4-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="875c4-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="875c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875c4-127">**Teclado de \_ Msvm**</span><span class="sxs-lookup"><span data-stu-id="875c4-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




