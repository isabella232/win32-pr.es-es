---
description: 'Método IShellDispatch2.ServiceStop: detiene un servicio con nombre.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Método IShellDispatch2.ServiceStop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117033"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="96709-103">Método IShellDispatch2.ServiceStop</span><span class="sxs-lookup"><span data-stu-id="96709-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="96709-104">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="96709-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="96709-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96709-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="96709-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96709-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96709-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="96709-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96709-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="96709-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="96709-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="96709-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="96709-110">*vPersistent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="96709-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96709-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="96709-111">Type: **Variant**</span></span>

<span data-ttu-id="96709-112">Establezca en **true para** que el administrador de control de servicios haya iniciado el servicio cuando se llame a [**ServiceStart.**](ishelldispatch2-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="96709-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="96709-113">Para dejar la configuración del servicio sin cambios, establezca *vPersistent* en **false.**</span><span class="sxs-lookup"><span data-stu-id="96709-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96709-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96709-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="96709-115">JScript</span><span class="sxs-lookup"><span data-stu-id="96709-115">JScript</span></span>

<span data-ttu-id="96709-116">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="96709-116">Type: **Variant\***</span></span>

<span data-ttu-id="96709-117">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="96709-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="96709-118">VB</span><span class="sxs-lookup"><span data-stu-id="96709-118">VB</span></span>

<span data-ttu-id="96709-119">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="96709-119">Type: **Variant\***</span></span>

<span data-ttu-id="96709-120">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="96709-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96709-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96709-121">Remarks</span></span>

<span data-ttu-id="96709-122">Este método se implementa y se accede a través del [**método Shell.ServiceStop.**](./shell-servicestop.md)</span><span class="sxs-lookup"><span data-stu-id="96709-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="96709-123">El método devuelve **false** si el servicio ya se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="96709-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="96709-124">Antes de llamar a este método, puede llamar a [**Shell.IsServiceRunning para**](./shell-isservicerunning.md) determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="96709-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="96709-125">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="96709-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="96709-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96709-126">Examples</span></span>

<span data-ttu-id="96709-127">En los ejemplos siguientes se muestra el uso de **ServiceStop para** detener el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="96709-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="96709-128">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="96709-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="96709-129">Jscript:</span><span class="sxs-lookup"><span data-stu-id="96709-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="96709-130">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="96709-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="96709-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96709-131">Requirements</span></span>



| <span data-ttu-id="96709-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="96709-132">Requirement</span></span> | <span data-ttu-id="96709-133">Valor</span><span class="sxs-lookup"><span data-stu-id="96709-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96709-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96709-134">Minimum supported client</span></span><br/> | <span data-ttu-id="96709-135">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="96709-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96709-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96709-136">Minimum supported server</span></span><br/> | <span data-ttu-id="96709-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="96709-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="96709-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96709-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="96709-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="96709-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="96709-140">Idl</span><span class="sxs-lookup"><span data-stu-id="96709-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96709-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="96709-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="96709-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96709-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96709-143"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="96709-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
