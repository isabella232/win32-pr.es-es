---
description: Solicita que el servicio de controlador del sistema actualice su estado al administrador de servicios.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Método InterrogateService de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152989"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="0b49c-103">Método InterrogateService de la \_ clase SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="0b49c-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="0b49c-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio de controlador del sistema actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="0b49c-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="0b49c-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0b49c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b49c-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b49c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b49c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b49c-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="0b49c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b49c-108">Parameters</span></span>

<span data-ttu-id="0b49c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0b49c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b49c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b49c-110">Return value</span></span>

<span data-ttu-id="0b49c-111">Devuelve un valor de 0 (cero) si se aceptó la solicitud de **InterrogateService** , 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0b49c-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b49c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b49c-112">Requirements</span></span>



| <span data-ttu-id="0b49c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b49c-113">Requirement</span></span> | <span data-ttu-id="0b49c-114">Value</span><span class="sxs-lookup"><span data-stu-id="0b49c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b49c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b49c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0b49c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b49c-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b49c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b49c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0b49c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b49c-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b49c-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b49c-119">Namespace</span></span><br/>                | <span data-ttu-id="0b49c-120">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b49c-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b49c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="0b49c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b49c-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b49c-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b49c-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b49c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b49c-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b49c-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b49c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b49c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b49c-126">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="0b49c-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="0b49c-127">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b49c-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b49c-128">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="0b49c-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

