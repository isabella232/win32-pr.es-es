---
description: Intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000763"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="9e97b-103">Método UserControlService de la \_ clase SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="9e97b-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="9e97b-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e97b-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="9e97b-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9e97b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9e97b-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9e97b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e97b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e97b-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="9e97b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e97b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e97b-109">*ControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e97b-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e97b-110">Especifica los valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="9e97b-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e97b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e97b-111">Return value</span></span>

<span data-ttu-id="9e97b-112">Devuelve un valor de 0 (cero) si se aceptó la solicitud **UserControlService** , 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9e97b-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e97b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e97b-113">Requirements</span></span>



| <span data-ttu-id="9e97b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e97b-114">Requirement</span></span> | <span data-ttu-id="9e97b-115">Value</span><span class="sxs-lookup"><span data-stu-id="9e97b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e97b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e97b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e97b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e97b-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e97b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e97b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e97b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e97b-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e97b-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9e97b-120">Namespace</span></span><br/>                | <span data-ttu-id="9e97b-121">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9e97b-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e97b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="9e97b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e97b-123"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e97b-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e97b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e97b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e97b-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e97b-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e97b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e97b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e97b-127">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e97b-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9e97b-128">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="9e97b-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

