---
description: Bloquea y desbloquea los medios en un dispositivo de acceso que se puede cambiar.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Método LockMedia de la clase CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083541"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="a08d7-103">Método LockMedia de la \_ clase MediaAccessDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="a08d7-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="a08d7-104">Bloquea y desbloquea los medios en un dispositivo de acceso que se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="a08d7-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a08d7-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="a08d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a08d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08d7-107">*Bloquear* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a08d7-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d7-108">Si **es true**, bloquea los medios.</span><span class="sxs-lookup"><span data-stu-id="a08d7-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="a08d7-109">Si **es false**, libera el medio.</span><span class="sxs-lookup"><span data-stu-id="a08d7-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08d7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a08d7-110">Return value</span></span>

<span data-ttu-id="a08d7-111">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a08d7-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08d7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a08d7-112">Requirements</span></span>



| <span data-ttu-id="a08d7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a08d7-113">Requirement</span></span> | <span data-ttu-id="a08d7-114">Value</span><span class="sxs-lookup"><span data-stu-id="a08d7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08d7-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a08d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a08d7-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a08d7-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a08d7-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a08d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a08d7-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a08d7-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a08d7-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a08d7-119">Namespace</span></span><br/>                | <span data-ttu-id="a08d7-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a08d7-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a08d7-121">MOF</span><span class="sxs-lookup"><span data-stu-id="a08d7-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a08d7-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a08d7-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a08d7-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a08d7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08d7-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a08d7-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a08d7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a08d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08d7-126">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a08d7-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




