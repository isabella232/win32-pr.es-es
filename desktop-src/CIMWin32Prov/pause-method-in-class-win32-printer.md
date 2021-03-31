---
description: Pone en pausa la cola de impresión.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Método PAUSE de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423471"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="3add5-103">Método PAUSE de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="3add5-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="3add5-104">El método **pausar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) pone en pausa la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="3add5-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="3add5-105">No se puede imprimir ningún trabajo hasta que se reanude la cola.</span><span class="sxs-lookup"><span data-stu-id="3add5-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="3add5-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3add5-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3add5-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3add5-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3add5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3add5-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="3add5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3add5-109">Parameters</span></span>

<span data-ttu-id="3add5-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3add5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3add5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3add5-111">Return value</span></span>

<span data-ttu-id="3add5-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3add5-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3add5-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3add5-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3add5-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3add5-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3add5-115">**0**</span><span class="sxs-lookup"><span data-stu-id="3add5-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3add5-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="3add5-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="3add5-117">**5**</span><span class="sxs-lookup"><span data-stu-id="3add5-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3add5-118">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="3add5-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3add5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3add5-119">Requirements</span></span>



| <span data-ttu-id="3add5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3add5-120">Requirement</span></span> | <span data-ttu-id="3add5-121">Value</span><span class="sxs-lookup"><span data-stu-id="3add5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3add5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3add5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3add5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3add5-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="3add5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3add5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3add5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3add5-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="3add5-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3add5-126">Namespace</span></span><br/>                | <span data-ttu-id="3add5-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3add5-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="3add5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="3add5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3add5-129"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3add5-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="3add5-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3add5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3add5-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3add5-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3add5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3add5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3add5-133">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="3add5-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3add5-134">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="3add5-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="3add5-135">**Método Resume**</span><span class="sxs-lookup"><span data-stu-id="3add5-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

