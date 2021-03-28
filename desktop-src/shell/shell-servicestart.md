---
description: Inicia un servicio con nombre.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Método Shell. ServiceStart (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909878"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="4892d-103">Shell. ServiceStart (método)</span><span class="sxs-lookup"><span data-stu-id="4892d-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="4892d-104">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="4892d-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4892d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4892d-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="4892d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4892d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4892d-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4892d-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4892d-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4892d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4892d-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="4892d-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="4892d-110">*vPersistent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4892d-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4892d-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="4892d-111">Type: **Variant**</span></span>

<span data-ttu-id="4892d-112">Establézcalo en **true** para que el servicio se inicie automáticamente por el administrador de control de servicios durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="4892d-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="4892d-113">Establézcalo en **false** para dejar la configuración del servicio sin cambios.</span><span class="sxs-lookup"><span data-stu-id="4892d-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4892d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4892d-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4892d-115">JScript</span><span class="sxs-lookup"><span data-stu-id="4892d-115">JScript</span></span>

<span data-ttu-id="4892d-116">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="4892d-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="4892d-117">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4892d-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="4892d-118">VB</span><span class="sxs-lookup"><span data-stu-id="4892d-118">VB</span></span>

<span data-ttu-id="4892d-119">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="4892d-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="4892d-120">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4892d-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4892d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4892d-121">Remarks</span></span>

<span data-ttu-id="4892d-122">El método devuelve **false** si el servicio ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="4892d-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="4892d-123">Antes de llamar a este método, puede llamar a [**Shell. IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="4892d-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="4892d-124">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4892d-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="4892d-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4892d-125">Examples</span></span>

<span data-ttu-id="4892d-126">En los siguientes ejemplos se muestra el uso de **ServiceStart** para iniciar el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="4892d-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="4892d-127">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="4892d-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="4892d-128">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4892d-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="4892d-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="4892d-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="4892d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4892d-130">Requirements</span></span>



| <span data-ttu-id="4892d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4892d-131">Requirement</span></span> | <span data-ttu-id="4892d-132">Value</span><span class="sxs-lookup"><span data-stu-id="4892d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4892d-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4892d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4892d-134">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4892d-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4892d-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4892d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4892d-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4892d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4892d-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4892d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4892d-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4892d-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4892d-139">IDL</span><span class="sxs-lookup"><span data-stu-id="4892d-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4892d-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4892d-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4892d-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4892d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4892d-142"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4892d-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
