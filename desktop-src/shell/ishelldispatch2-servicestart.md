---
description: Inicia un servicio con nombre.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Método IShellDispatch2. ServiceStart (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984674"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="5f35d-103">IShellDispatch2. ServiceStart, método</span><span class="sxs-lookup"><span data-stu-id="5f35d-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="5f35d-104">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="5f35d-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f35d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f35d-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="5f35d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f35d-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f35d-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f35d-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5f35d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5f35d-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="5f35d-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f35d-110">*vPersistent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f35d-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f35d-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="5f35d-111">Type: **Variant**</span></span>

<span data-ttu-id="5f35d-112">Establézcalo en **true** para que el servicio se inicie automáticamente por el administrador de control de servicios durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5f35d-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="5f35d-113">Establézcalo en **false** para dejar la configuración del servicio sin cambios.</span><span class="sxs-lookup"><span data-stu-id="5f35d-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f35d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f35d-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5f35d-115">JScript</span><span class="sxs-lookup"><span data-stu-id="5f35d-115">JScript</span></span>

<span data-ttu-id="5f35d-116">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="5f35d-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="5f35d-117">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5f35d-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="5f35d-118">VB</span><span class="sxs-lookup"><span data-stu-id="5f35d-118">VB</span></span>

<span data-ttu-id="5f35d-119">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="5f35d-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="5f35d-120">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5f35d-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f35d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f35d-121">Remarks</span></span>

<span data-ttu-id="5f35d-122">Este método se implementa y se obtiene acceso a él a través del método [**Shell. ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="5f35d-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="5f35d-123">El método devuelve **false** si el servicio ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="5f35d-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="5f35d-124">Antes de llamar a este método, puede llamar a [**Shell. IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="5f35d-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="5f35d-125">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5f35d-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="5f35d-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5f35d-126">Examples</span></span>

<span data-ttu-id="5f35d-127">En los siguientes ejemplos se muestra el uso de **ServiceStart** para iniciar el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="5f35d-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="5f35d-128">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="5f35d-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="5f35d-129">JScript.net</span><span class="sxs-lookup"><span data-stu-id="5f35d-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="5f35d-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="5f35d-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5f35d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f35d-131">Requirements</span></span>



| <span data-ttu-id="5f35d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f35d-132">Requirement</span></span> | <span data-ttu-id="5f35d-133">Value</span><span class="sxs-lookup"><span data-stu-id="5f35d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f35d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f35d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f35d-135">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f35d-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f35d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f35d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f35d-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f35d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5f35d-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f35d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f35d-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f35d-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5f35d-140">IDL</span><span class="sxs-lookup"><span data-stu-id="5f35d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f35d-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f35d-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5f35d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f35d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f35d-143"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5f35d-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
