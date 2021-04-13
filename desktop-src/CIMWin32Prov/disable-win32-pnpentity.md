---
description: Deshabilita este dispositivo Plug and Play.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Método Disable de la clase Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538698"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="c9832-103">Método Disable de la \_ clase Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="c9832-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="c9832-104">Deshabilita este dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="c9832-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9832-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9832-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="c9832-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9832-107">*rebootNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9832-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9832-108">Indica si es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="c9832-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9832-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9832-109">Requirements</span></span>



| <span data-ttu-id="c9832-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9832-110">Requirement</span></span> | <span data-ttu-id="c9832-111">Value</span><span class="sxs-lookup"><span data-stu-id="c9832-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9832-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9832-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c9832-113">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9832-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9832-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9832-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c9832-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9832-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="c9832-116">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9832-116">Namespace</span></span><br/>                | <span data-ttu-id="c9832-117">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c9832-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9832-118">MOF</span><span class="sxs-lookup"><span data-stu-id="c9832-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9832-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9832-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9832-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9832-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9832-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9832-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9832-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9832-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9832-123">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="c9832-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




