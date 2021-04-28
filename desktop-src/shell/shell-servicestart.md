---
description: 'Método Shell.ServiceStart: inicia un servicio con nombre.'
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Método Shell.ServiceStart (Shldisp.h)
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
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083753"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="fcd16-103">Método Shell.ServiceStart</span><span class="sxs-lookup"><span data-stu-id="fcd16-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="fcd16-104">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="fcd16-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcd16-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="fcd16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcd16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd16-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fcd16-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd16-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fcd16-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fcd16-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="fcd16-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="fcd16-110">*vPersistent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fcd16-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd16-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="fcd16-111">Type: **Variant**</span></span>

<span data-ttu-id="fcd16-112">Establezca en **true para** que el administrador de control de servicios inicie automáticamente el servicio durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="fcd16-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="fcd16-113">Establezca en **false** para dejar la configuración del servicio sin cambios.</span><span class="sxs-lookup"><span data-stu-id="fcd16-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd16-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcd16-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fcd16-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fcd16-115">JScript</span></span>

<span data-ttu-id="fcd16-116">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="fcd16-116">Type: **Variant\***</span></span>

<span data-ttu-id="fcd16-117">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcd16-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fcd16-118">VB</span><span class="sxs-lookup"><span data-stu-id="fcd16-118">VB</span></span>

<span data-ttu-id="fcd16-119">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="fcd16-119">Type: **Variant\***</span></span>

<span data-ttu-id="fcd16-120">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcd16-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd16-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcd16-121">Remarks</span></span>

<span data-ttu-id="fcd16-122">El método devuelve **false** si el servicio ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="fcd16-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="fcd16-123">Antes de llamar a este método, puede llamar a [**Shell.IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="fcd16-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="fcd16-124">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fcd16-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fcd16-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fcd16-125">Examples</span></span>

<span data-ttu-id="fcd16-126">En los ejemplos siguientes se muestra el uso de **ServiceStart** para iniciar el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="fcd16-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="fcd16-127">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="fcd16-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fcd16-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="fcd16-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="fcd16-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="fcd16-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fcd16-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcd16-130">Requirements</span></span>



| <span data-ttu-id="fcd16-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd16-131">Requirement</span></span> | <span data-ttu-id="fcd16-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fcd16-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd16-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd16-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd16-134">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="fcd16-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcd16-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd16-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd16-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcd16-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fcd16-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcd16-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd16-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd16-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fcd16-139">Idl</span><span class="sxs-lookup"><span data-stu-id="fcd16-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fcd16-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="fcd16-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fcd16-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcd16-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd16-142"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fcd16-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
