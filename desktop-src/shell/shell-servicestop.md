---
description: Detiene un servicio con nombre.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Método Shell. ServiceStop (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277406"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="d76f6-103">Shell. ServiceStop (método)</span><span class="sxs-lookup"><span data-stu-id="d76f6-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="d76f6-104">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="d76f6-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d76f6-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="d76f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d76f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76f6-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d76f6-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76f6-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d76f6-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d76f6-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d76f6-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="d76f6-110">*vPersistent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d76f6-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76f6-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="d76f6-111">Type: **Variant**</span></span>

<span data-ttu-id="d76f6-112">Establézcalo en **true** para que el servicio se inicie por el administrador de control de servicios cuando se llame a [**ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="d76f6-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="d76f6-113">Para dejar la configuración del servicio sin modificar, establezca *vPersistent* en **false**.</span><span class="sxs-lookup"><span data-stu-id="d76f6-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76f6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d76f6-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d76f6-115">JScript</span><span class="sxs-lookup"><span data-stu-id="d76f6-115">JScript</span></span>

<span data-ttu-id="d76f6-116">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d76f6-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="d76f6-117">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d76f6-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="d76f6-118">VB</span><span class="sxs-lookup"><span data-stu-id="d76f6-118">VB</span></span>

<span data-ttu-id="d76f6-119">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d76f6-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="d76f6-120">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d76f6-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76f6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d76f6-121">Remarks</span></span>

<span data-ttu-id="d76f6-122">El método devuelve **false** si el servicio ya se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="d76f6-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="d76f6-123">Antes de llamar a este método, puede llamar a [**Shell. IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="d76f6-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="d76f6-124">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d76f6-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d76f6-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d76f6-125">Examples</span></span>

<span data-ttu-id="d76f6-126">En los siguientes ejemplos se muestra el uso de **ServiceStop** para detener el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="d76f6-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="d76f6-127">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="d76f6-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="d76f6-128">JScript.net</span><span class="sxs-lookup"><span data-stu-id="d76f6-128">JScript:</span></span>


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



<span data-ttu-id="d76f6-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="d76f6-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d76f6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d76f6-130">Requirements</span></span>



| <span data-ttu-id="d76f6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d76f6-131">Requirement</span></span> | <span data-ttu-id="d76f6-132">Value</span><span class="sxs-lookup"><span data-stu-id="d76f6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76f6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d76f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d76f6-134">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d76f6-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d76f6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d76f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d76f6-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d76f6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d76f6-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d76f6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76f6-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d76f6-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d76f6-139">IDL</span><span class="sxs-lookup"><span data-stu-id="d76f6-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d76f6-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d76f6-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d76f6-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d76f6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d76f6-142"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d76f6-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
