---
description: Habilita el adaptador de red.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Método enable de la clase Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274921"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="bbf63-103">Método enable de la \_ clase Win32 el adaptador</span><span class="sxs-lookup"><span data-stu-id="bbf63-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="bbf63-104">El método **enable** habilita el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="bbf63-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbf63-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="bbf63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbf63-106">Parameters</span></span>

<span data-ttu-id="bbf63-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bbf63-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbf63-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbf63-108">Return value</span></span>

<span data-ttu-id="bbf63-109">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bbf63-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="bbf63-110">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="bbf63-110">Any other number indicates an error.</span></span> <span data-ttu-id="bbf63-111">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bbf63-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf63-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbf63-112">Remarks</span></span>

<span data-ttu-id="bbf63-113">Puede experimentar dificultades con este método si la aplicación no administra el acceso a privilidges.</span><span class="sxs-lookup"><span data-stu-id="bbf63-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="bbf63-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bbf63-114">Examples</span></span>

<span data-ttu-id="bbf63-115">En el siguiente ejemplo de script de Visual Basic se habilita el primer adaptador de red y se muestra el estado de la propiedad **NetEnabled** .</span><span class="sxs-lookup"><span data-stu-id="bbf63-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="bbf63-116">Para obtener más información, consulte [**SWbemObjectSet. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span><span class="sxs-lookup"><span data-stu-id="bbf63-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="bbf63-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbf63-117">Requirements</span></span>



| <span data-ttu-id="bbf63-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbf63-118">Requirement</span></span> | <span data-ttu-id="bbf63-119">Value</span><span class="sxs-lookup"><span data-stu-id="bbf63-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf63-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbf63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf63-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbf63-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbf63-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbf63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf63-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbf63-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbf63-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bbf63-124">Namespace</span></span><br/>                | <span data-ttu-id="bbf63-125">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bbf63-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bbf63-126">MOF</span><span class="sxs-lookup"><span data-stu-id="bbf63-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbf63-127"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbf63-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbf63-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbf63-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbf63-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf63-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf63-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbf63-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf63-131">**Adaptador de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="bbf63-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="bbf63-132">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="bbf63-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="bbf63-133">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="bbf63-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

