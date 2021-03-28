---
description: Coloca el objeto de usuario especificado junto a la línea para la resolución de nombres.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Método DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540467"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="d190f-103">DiskQuotaControl. GiveUserNameResolutionPriority, método</span><span class="sxs-lookup"><span data-stu-id="d190f-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="d190f-104">Coloca el objeto de usuario especificado junto a la línea para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d190f-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="d190f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d190f-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="d190f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d190f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d190f-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="d190f-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="d190f-108">Tipo: **Object**</span><span class="sxs-lookup"><span data-stu-id="d190f-108">Type: **Object**</span></span>

<span data-ttu-id="d190f-109">Expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="d190f-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d190f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d190f-110">Return value</span></span>

<span data-ttu-id="d190f-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d190f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d190f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d190f-112">Remarks</span></span>

<span data-ttu-id="d190f-113">Si la resolución de nombres asincrónica está habilitada, los objetos de usuario se colocan en una cola.</span><span class="sxs-lookup"><span data-stu-id="d190f-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="d190f-114">De forma predeterminada, se les presta servicio en el orden en que se colocan en la cola.</span><span class="sxs-lookup"><span data-stu-id="d190f-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="d190f-115">El método **GiveUserNameResolutionPriority** mueve un objeto al principio de la cola para que sea el siguiente en la línea que se va a atender.</span><span class="sxs-lookup"><span data-stu-id="d190f-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="d190f-116">Use la propiedad [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para habilitar la resolución de nombres asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d190f-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="d190f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d190f-117">Requirements</span></span>



| <span data-ttu-id="d190f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d190f-118">Requirement</span></span> | <span data-ttu-id="d190f-119">Value</span><span class="sxs-lookup"><span data-stu-id="d190f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d190f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d190f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d190f-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d190f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d190f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d190f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d190f-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d190f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d190f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d190f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d190f-125"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="d190f-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="d190f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d190f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d190f-127"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d190f-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d190f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d190f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d190f-129">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="d190f-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




