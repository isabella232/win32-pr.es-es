---
description: 'Método IShellDispatch2.IsServiceRunning: devuelve un valor que indica si se está ejecutando un servicio determinado.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Método IShellDispatch2.IsServiceRunning (Shldisp.h)
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
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117093"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="982a4-103">Método IShellDispatch2.IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="982a4-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="982a4-104">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="982a4-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="982a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="982a4-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="982a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="982a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="982a4-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="982a4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="982a4-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="982a4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="982a4-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="982a4-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="982a4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="982a4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="982a4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="982a4-111">JScript</span></span>

<span data-ttu-id="982a4-112">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="982a4-112">Type: **Variant\***</span></span>

<span data-ttu-id="982a4-113">Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="982a4-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="982a4-114">VB</span><span class="sxs-lookup"><span data-stu-id="982a4-114">VB</span></span>

<span data-ttu-id="982a4-115">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="982a4-115">Type: **Variant\***</span></span>

<span data-ttu-id="982a4-116">Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="982a4-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="982a4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="982a4-117">Remarks</span></span>

<span data-ttu-id="982a4-118">Este método se implementa y se accede a través del [**método Shell.IsServiceRunning.**](./shell-isservicerunning.md)</span><span class="sxs-lookup"><span data-stu-id="982a4-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="982a4-119">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="982a4-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="982a4-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="982a4-120">Examples</span></span>

<span data-ttu-id="982a4-121">En los ejemplos siguientes se muestra el uso de **IsServiceRunning para** determinar si el servicio Themes se está ejecutando para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="982a4-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="982a4-122">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="982a4-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="982a4-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="982a4-123">JScript:</span></span>


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



<span data-ttu-id="982a4-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="982a4-124">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="982a4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="982a4-125">Requirements</span></span>



| <span data-ttu-id="982a4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="982a4-126">Requirement</span></span> | <span data-ttu-id="982a4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="982a4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="982a4-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="982a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="982a4-129">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="982a4-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="982a4-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="982a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="982a4-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="982a4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="982a4-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="982a4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="982a4-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="982a4-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="982a4-134">Idl</span><span class="sxs-lookup"><span data-stu-id="982a4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="982a4-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="982a4-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="982a4-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="982a4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="982a4-137"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="982a4-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
