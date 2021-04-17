---
description: Habilita este Plug and Play dispositivo.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Método enable de la clase Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659489"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="4816b-103">Método enable de la \_ clase Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="4816b-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="4816b-104">Habilita este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4816b-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4816b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4816b-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4816b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4816b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4816b-107">*rebootNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4816b-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4816b-108">Indica si es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="4816b-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4816b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4816b-109">Requirements</span></span>



| <span data-ttu-id="4816b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4816b-110">Requirement</span></span> | <span data-ttu-id="4816b-111">Value</span><span class="sxs-lookup"><span data-stu-id="4816b-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4816b-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4816b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4816b-113">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4816b-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4816b-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4816b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4816b-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4816b-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="4816b-116">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4816b-116">Namespace</span></span><br/>                | <span data-ttu-id="4816b-117">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4816b-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4816b-118">MOF</span><span class="sxs-lookup"><span data-stu-id="4816b-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4816b-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4816b-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4816b-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4816b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4816b-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4816b-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4816b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4816b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4816b-123">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="4816b-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




