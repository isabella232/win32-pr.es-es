---
description: 'Método Delete de la Win32_SystemDriver clase : el&\# 8194; El método de clase WMI elimina un servicio existente.'
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Método Delete de la Win32_SystemDriver clase
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
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097093"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="53930-103">Método Delete de la clase \_ SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="53930-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="53930-104">El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="53930-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="53930-105">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="53930-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="53930-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="53930-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="53930-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53930-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="53930-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53930-108">Parameters</span></span>

<span data-ttu-id="53930-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53930-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53930-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53930-110">Return value</span></span>

<span data-ttu-id="53930-111">Devuelve un valor de 0 (cero) si el servicio se eliminó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="53930-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="53930-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53930-112">Requirements</span></span>



| <span data-ttu-id="53930-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="53930-113">Requirement</span></span> | <span data-ttu-id="53930-114">Valor</span><span class="sxs-lookup"><span data-stu-id="53930-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53930-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53930-115">Minimum supported client</span></span><br/> | <span data-ttu-id="53930-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53930-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53930-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53930-117">Minimum supported server</span></span><br/> | <span data-ttu-id="53930-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53930-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53930-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53930-119">Namespace</span></span><br/>                | <span data-ttu-id="53930-120">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="53930-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53930-121">MOF</span><span class="sxs-lookup"><span data-stu-id="53930-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53930-122"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="53930-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53930-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53930-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53930-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53930-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53930-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53930-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="53930-126">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53930-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="53930-127">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="53930-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

