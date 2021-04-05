---
description: Obtiene las propiedades especificadas de este Plug and Play dispositivo.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Método GetDeviceProperties de la clase Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080161"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="442e9-103">Método GetDeviceProperties de la \_ clase PnPEntity de Win32</span><span class="sxs-lookup"><span data-stu-id="442e9-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="442e9-104">Obtiene las propiedades especificadas de este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="442e9-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="442e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="442e9-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="442e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="442e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442e9-107">*devicePropertyKeys* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="442e9-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="442e9-108">Propiedades que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="442e9-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="442e9-109">*deviceProperties* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="442e9-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="442e9-110">Las propiedades solicitadas en los subtipos adecuados de la clase abstracta [**\_ PnPDeviceProperty de Win32**](win32-pnpdeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="442e9-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="442e9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="442e9-111">Requirements</span></span>



| <span data-ttu-id="442e9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="442e9-112">Requirement</span></span> | <span data-ttu-id="442e9-113">Value</span><span class="sxs-lookup"><span data-stu-id="442e9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="442e9-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="442e9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="442e9-115">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="442e9-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="442e9-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="442e9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="442e9-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="442e9-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="442e9-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="442e9-118">Namespace</span></span><br/>                | <span data-ttu-id="442e9-119">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="442e9-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="442e9-120">MOF</span><span class="sxs-lookup"><span data-stu-id="442e9-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="442e9-121"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="442e9-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="442e9-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="442e9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="442e9-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="442e9-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="442e9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="442e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442e9-125">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="442e9-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




