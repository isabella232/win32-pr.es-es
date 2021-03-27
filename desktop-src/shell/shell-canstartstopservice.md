---
description: Determina si el usuario actual puede iniciar y detener el servicio con nombre.
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Método Shell. CanStartStopService (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002208"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="ea182-103">Shell. CanStartStopService (método)</span><span class="sxs-lookup"><span data-stu-id="ea182-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="ea182-104">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="ea182-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea182-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea182-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="ea182-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea182-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea182-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea182-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="ea182-108">Type: **String**</span></span>

<span data-ttu-id="ea182-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="ea182-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea182-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea182-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ea182-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ea182-111">JScript</span></span>

<span data-ttu-id="ea182-112">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="ea182-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="ea182-113">Devuelve _ *true*\* si el usuario puede iniciar y detener el servicio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ea182-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ea182-114">VB</span><span class="sxs-lookup"><span data-stu-id="ea182-114">VB</span></span>

<span data-ttu-id="ea182-115">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="ea182-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="ea182-116">Devuelve _ *true*\* si el usuario puede iniciar y detener el servicio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ea182-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea182-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea182-117">Remarks</span></span>

<span data-ttu-id="ea182-118">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ea182-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ea182-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ea182-119">Examples</span></span>

<span data-ttu-id="ea182-120">En los siguientes ejemplos se muestra el uso de **CanStartStopService** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="ea182-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="ea182-121">JScript.net</span><span class="sxs-lookup"><span data-stu-id="ea182-121">JScript:</span></span>


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



<span data-ttu-id="ea182-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="ea182-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ea182-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea182-123">Requirements</span></span>



| <span data-ttu-id="ea182-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea182-124">Requirement</span></span> | <span data-ttu-id="ea182-125">Value</span><span class="sxs-lookup"><span data-stu-id="ea182-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea182-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea182-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea182-127">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ea182-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea182-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea182-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea182-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea182-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ea182-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea182-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea182-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea182-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ea182-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ea182-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea182-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea182-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ea182-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea182-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea182-135"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ea182-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




