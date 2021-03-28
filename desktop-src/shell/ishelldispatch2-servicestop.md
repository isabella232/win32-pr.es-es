---
description: Detiene un servicio con nombre.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Método IShellDispatch2. ServiceStop (Shldisp. h)
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984670"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="d85f7-103">IShellDispatch2. ServiceStop, método</span><span class="sxs-lookup"><span data-stu-id="d85f7-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="d85f7-104">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="d85f7-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d85f7-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="d85f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d85f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85f7-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d85f7-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85f7-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d85f7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d85f7-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d85f7-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="d85f7-110">*vPersistent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d85f7-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85f7-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="d85f7-111">Type: **Variant**</span></span>

<span data-ttu-id="d85f7-112">Establézcalo en **true** para que el servicio se inicie por el administrador de control de servicios cuando se llame a [**ServiceStart**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="d85f7-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="d85f7-113">Para dejar la configuración del servicio sin modificar, establezca *vPersistent* en **false**.</span><span class="sxs-lookup"><span data-stu-id="d85f7-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85f7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d85f7-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d85f7-115">JScript</span><span class="sxs-lookup"><span data-stu-id="d85f7-115">JScript</span></span>

<span data-ttu-id="d85f7-116">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d85f7-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="d85f7-117">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d85f7-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="d85f7-118">VB</span><span class="sxs-lookup"><span data-stu-id="d85f7-118">VB</span></span>

<span data-ttu-id="d85f7-119">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d85f7-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="d85f7-120">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d85f7-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d85f7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d85f7-121">Remarks</span></span>

<span data-ttu-id="d85f7-122">Este método se implementa y se obtiene acceso a él a través del método [**Shell. ServiceStop**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="d85f7-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="d85f7-123">El método devuelve **false** si el servicio ya se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="d85f7-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="d85f7-124">Antes de llamar a este método, puede llamar a [**Shell. IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="d85f7-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="d85f7-125">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d85f7-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d85f7-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d85f7-126">Examples</span></span>

<span data-ttu-id="d85f7-127">En los siguientes ejemplos se muestra el uso de **ServiceStop** para detener el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="d85f7-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="d85f7-128">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="d85f7-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="d85f7-129">JScript.net</span><span class="sxs-lookup"><span data-stu-id="d85f7-129">JScript:</span></span>


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



<span data-ttu-id="d85f7-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="d85f7-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d85f7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d85f7-131">Requirements</span></span>



| <span data-ttu-id="d85f7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d85f7-132">Requirement</span></span> | <span data-ttu-id="d85f7-133">Value</span><span class="sxs-lookup"><span data-stu-id="d85f7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d85f7-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85f7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d85f7-135">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d85f7-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d85f7-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85f7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d85f7-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d85f7-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d85f7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d85f7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d85f7-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d85f7-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d85f7-140">IDL</span><span class="sxs-lookup"><span data-stu-id="d85f7-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d85f7-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d85f7-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d85f7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d85f7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d85f7-143"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d85f7-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
