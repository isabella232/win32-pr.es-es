---
description: Devuelve un valor que indica si se está ejecutando un servicio determinado.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Método IShellDispatch2. IsServiceRunning (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984683"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="dec69-103">IShellDispatch2. IsServiceRunning, método</span><span class="sxs-lookup"><span data-stu-id="dec69-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="dec69-104">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="dec69-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dec69-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="dec69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dec69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec69-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dec69-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec69-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="dec69-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="dec69-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="dec69-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec69-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dec69-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dec69-111">JScript</span><span class="sxs-lookup"><span data-stu-id="dec69-111">JScript</span></span>

<span data-ttu-id="dec69-112">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="dec69-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="dec69-113">Devuelve _ *true*\* si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dec69-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="dec69-114">VB</span><span class="sxs-lookup"><span data-stu-id="dec69-114">VB</span></span>

<span data-ttu-id="dec69-115">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="dec69-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="dec69-116">Devuelve _ *true*\* si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dec69-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec69-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dec69-117">Remarks</span></span>

<span data-ttu-id="dec69-118">Este método se implementa y se obtiene acceso a él a través del método [**Shell. IsServiceRunning**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="dec69-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="dec69-119">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dec69-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="dec69-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dec69-120">Examples</span></span>

<span data-ttu-id="dec69-121">En los siguientes ejemplos se muestra el uso de **IsServiceRunning** para determinar si el servicio themes se está ejecutando para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dec69-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="dec69-122">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="dec69-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="dec69-123">JScript.net</span><span class="sxs-lookup"><span data-stu-id="dec69-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="dec69-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="dec69-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="dec69-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec69-125">Requirements</span></span>



| <span data-ttu-id="dec69-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec69-126">Requirement</span></span> | <span data-ttu-id="dec69-127">Value</span><span class="sxs-lookup"><span data-stu-id="dec69-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec69-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dec69-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dec69-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dec69-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dec69-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dec69-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dec69-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dec69-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dec69-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dec69-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec69-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec69-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dec69-134">IDL</span><span class="sxs-lookup"><span data-stu-id="dec69-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec69-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec69-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dec69-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dec69-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec69-137"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dec69-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
