---
description: 'Método IShellDispatch2.CanStartStopService: determina si el usuario actual puede iniciar y detener el servicio con nombre.'
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Método IShellDispatch2.CanStartStopService (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117133"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="1e892-103">Método IShellDispatch2.CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="1e892-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="1e892-104">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="1e892-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e892-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e892-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="1e892-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e892-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1e892-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e892-108">Tipo: **Cadena**</span><span class="sxs-lookup"><span data-stu-id="1e892-108">Type: **String**</span></span>

<span data-ttu-id="1e892-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="1e892-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e892-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e892-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1e892-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1e892-111">JScript</span></span>

<span data-ttu-id="1e892-112">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1e892-112">Type: **Variant\***</span></span>

<span data-ttu-id="1e892-113">Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1e892-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="1e892-114">VB</span><span class="sxs-lookup"><span data-stu-id="1e892-114">VB</span></span>

<span data-ttu-id="1e892-115">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1e892-115">Type: **Variant\***</span></span>

<span data-ttu-id="1e892-116">Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1e892-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e892-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e892-117">Remarks</span></span>

<span data-ttu-id="1e892-118">Este método se implementa y se accede a través del [**método Shell.CanStartStopService.**](./shell-canstartstopservice.md)</span><span class="sxs-lookup"><span data-stu-id="1e892-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="1e892-119">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e892-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1e892-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1e892-120">Examples</span></span>

<span data-ttu-id="1e892-121">En los ejemplos siguientes se muestra el **uso de CanStartStopService** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="1e892-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="1e892-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="1e892-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="1e892-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="1e892-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="1e892-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e892-124">Requirements</span></span>



| <span data-ttu-id="1e892-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e892-125">Requirement</span></span> | <span data-ttu-id="1e892-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1e892-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e892-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e892-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1e892-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="1e892-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e892-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e892-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1e892-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e892-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e892-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e892-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e892-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e892-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1e892-133">Idl</span><span class="sxs-lookup"><span data-stu-id="1e892-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e892-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e892-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1e892-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e892-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e892-136"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1e892-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
