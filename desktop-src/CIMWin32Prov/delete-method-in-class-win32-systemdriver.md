---
description: La eliminación&\# 8194; El método de clase WMI elimina un servicio existente.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 807fa6090fe2e088fb3900feb7f2068751ad2df6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907278"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="ef0ed-103">Método Delete de la \_ clase Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="ef0ed-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="ef0ed-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="ef0ed-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ef0ed-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef0ed-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef0ed-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0ed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef0ed-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ef0ed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef0ed-108">Parameters</span></span>

<span data-ttu-id="ef0ed-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef0ed-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef0ed-110">Return value</span></span>

<span data-ttu-id="ef0ed-111">Devuelve un valor de 0 (cero) si el servicio se eliminó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="ef0ed-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0ed-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0ed-112">Requirements</span></span>



| <span data-ttu-id="ef0ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0ed-113">Requirement</span></span> | <span data-ttu-id="ef0ed-114">Value</span><span class="sxs-lookup"><span data-stu-id="ef0ed-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0ed-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0ed-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0ed-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef0ed-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef0ed-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0ed-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0ed-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef0ed-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef0ed-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef0ed-119">Namespace</span></span><br/>                | <span data-ttu-id="ef0ed-120">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ef0ed-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef0ed-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0ed-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0ed-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef0ed-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0ed-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef0ed-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0ed-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0ed-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0ed-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef0ed-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef0ed-126">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef0ed-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef0ed-127">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="ef0ed-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

