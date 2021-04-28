---
description: 'Método Shell.CanStartStopService: determina si el usuario actual puede iniciar y detener el servicio con nombre.'
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Método Shell.CanStartStopService (Shldisp.h)
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
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083693"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="dbc41-103">Método Shell.CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="dbc41-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="dbc41-104">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="dbc41-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbc41-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="dbc41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbc41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc41-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dbc41-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc41-108">Tipo: **Cadena**</span><span class="sxs-lookup"><span data-stu-id="dbc41-108">Type: **String**</span></span>

<span data-ttu-id="dbc41-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="dbc41-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc41-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbc41-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dbc41-111">JScript</span><span class="sxs-lookup"><span data-stu-id="dbc41-111">JScript</span></span>

<span data-ttu-id="dbc41-112">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="dbc41-112">Type: **Variant\***</span></span>

<span data-ttu-id="dbc41-113">Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dbc41-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="dbc41-114">VB</span><span class="sxs-lookup"><span data-stu-id="dbc41-114">VB</span></span>

<span data-ttu-id="dbc41-115">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="dbc41-115">Type: **Variant\***</span></span>

<span data-ttu-id="dbc41-116">Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dbc41-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc41-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbc41-117">Remarks</span></span>

<span data-ttu-id="dbc41-118">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dbc41-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="dbc41-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dbc41-119">Examples</span></span>

<span data-ttu-id="dbc41-120">En los ejemplos siguientes se muestra el **uso de CanStartStopService** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="dbc41-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="dbc41-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="dbc41-121">JScript:</span></span>


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



<span data-ttu-id="dbc41-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="dbc41-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="dbc41-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc41-123">Requirements</span></span>



| <span data-ttu-id="dbc41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc41-124">Requirement</span></span> | <span data-ttu-id="dbc41-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc41-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc41-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbc41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc41-127">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="dbc41-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbc41-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbc41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc41-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbc41-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dbc41-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbc41-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc41-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc41-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dbc41-132">Idl</span><span class="sxs-lookup"><span data-stu-id="dbc41-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dbc41-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="dbc41-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dbc41-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbc41-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbc41-135"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc41-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




