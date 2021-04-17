---
description: Restablece el teclado virtual.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Método Reset de la clase Msvm_Keyboard
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
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669773"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="44180-103">Método Reset de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="44180-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="44180-104">Restablece el teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="44180-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="44180-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44180-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="44180-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44180-106">Parameters</span></span>

<span data-ttu-id="44180-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="44180-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44180-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44180-108">Return value</span></span>

<span data-ttu-id="44180-109">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="44180-109">A return value of zero indicates success.</span></span> <span data-ttu-id="44180-110">Un valor devuelto de uno indica un error porque no se admite el método.</span><span class="sxs-lookup"><span data-stu-id="44180-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="44180-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="44180-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44180-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="44180-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44180-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44180-113">Requirements</span></span>



| <span data-ttu-id="44180-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44180-114">Requirement</span></span> | <span data-ttu-id="44180-115">Value</span><span class="sxs-lookup"><span data-stu-id="44180-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44180-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44180-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44180-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="44180-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="44180-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44180-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44180-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44180-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="44180-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44180-120">Namespace</span></span><br/>                | <span data-ttu-id="44180-121">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="44180-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="44180-122">MOF</span><span class="sxs-lookup"><span data-stu-id="44180-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44180-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44180-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44180-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44180-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44180-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44180-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44180-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="44180-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44180-127">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="44180-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




