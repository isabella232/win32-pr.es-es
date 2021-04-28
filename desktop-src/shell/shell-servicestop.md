---
description: 'Método Shell.ServiceStop: detiene un servicio con nombre.'
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Método Shell.ServiceStop (Shldisp.h)
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
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104163"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="ca889-103">Método Shell.ServiceStop</span><span class="sxs-lookup"><span data-stu-id="ca889-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="ca889-104">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="ca889-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca889-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca889-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="ca889-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca889-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca889-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ca889-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca889-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ca889-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ca889-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="ca889-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca889-110">*vPersistent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ca889-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca889-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ca889-111">Type: **Variant**</span></span>

<span data-ttu-id="ca889-112">Establezca en **true** para que el administrador de control de servicios lo haya iniciado cuando se llame a [**ServiceStart.**](./shell-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="ca889-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="ca889-113">Para dejar la configuración del servicio sin cambios, *establezca vPersistent* en **false.**</span><span class="sxs-lookup"><span data-stu-id="ca889-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca889-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca889-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ca889-115">JScript</span><span class="sxs-lookup"><span data-stu-id="ca889-115">JScript</span></span>

<span data-ttu-id="ca889-116">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="ca889-116">Type: **Variant\***</span></span>

<span data-ttu-id="ca889-117">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ca889-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ca889-118">VB</span><span class="sxs-lookup"><span data-stu-id="ca889-118">VB</span></span>

<span data-ttu-id="ca889-119">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="ca889-119">Type: **Variant\***</span></span>

<span data-ttu-id="ca889-120">Devuelve **true si** se realiza correctamente; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ca889-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca889-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca889-121">Remarks</span></span>

<span data-ttu-id="ca889-122">El método devuelve **false** si el servicio ya se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="ca889-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="ca889-123">Antes de llamar a este método, puede llamar a [**Shell.IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="ca889-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="ca889-124">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ca889-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ca889-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ca889-125">Examples</span></span>

<span data-ttu-id="ca889-126">En los ejemplos siguientes se muestra el uso de **ServiceStop para** detener el servicio Messenger.</span><span class="sxs-lookup"><span data-stu-id="ca889-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="ca889-127">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="ca889-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ca889-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ca889-128">JScript:</span></span>


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



<span data-ttu-id="ca889-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ca889-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ca889-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca889-130">Requirements</span></span>



| <span data-ttu-id="ca889-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca889-131">Requirement</span></span> | <span data-ttu-id="ca889-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ca889-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca889-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca889-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ca889-134">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ca889-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca889-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca889-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ca889-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca889-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ca889-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca889-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca889-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ca889-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ca889-139">Idl</span><span class="sxs-lookup"><span data-stu-id="ca889-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca889-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca889-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ca889-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca889-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca889-142"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ca889-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
