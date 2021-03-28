---
description: Devuelve un valor que indica si se está ejecutando un servicio determinado.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Método Shell. IsServiceRunning (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909881"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="d57c9-103">Shell. IsServiceRunning (método)</span><span class="sxs-lookup"><span data-stu-id="d57c9-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="d57c9-104">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="d57c9-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d57c9-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="d57c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d57c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57c9-107">*sServiceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d57c9-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57c9-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d57c9-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d57c9-109">**Cadena** que contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d57c9-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57c9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d57c9-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d57c9-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d57c9-111">JScript</span></span>

<span data-ttu-id="d57c9-112">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d57c9-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="d57c9-113">Devuelve _ *true*\* si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d57c9-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="d57c9-114">VB</span><span class="sxs-lookup"><span data-stu-id="d57c9-114">VB</span></span>

<span data-ttu-id="d57c9-115">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d57c9-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="d57c9-116">Devuelve _ *true*\* si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d57c9-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57c9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d57c9-117">Remarks</span></span>

<span data-ttu-id="d57c9-118">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d57c9-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d57c9-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d57c9-119">Examples</span></span>

<span data-ttu-id="d57c9-120">En los siguientes ejemplos se muestra el uso de **IsServiceRunning** para determinar si el servicio themes se está ejecutando para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d57c9-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="d57c9-121">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="d57c9-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="d57c9-122">JScript.net</span><span class="sxs-lookup"><span data-stu-id="d57c9-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="d57c9-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="d57c9-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="d57c9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d57c9-124">Requirements</span></span>



| <span data-ttu-id="d57c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d57c9-125">Requirement</span></span> | <span data-ttu-id="d57c9-126">Value</span><span class="sxs-lookup"><span data-stu-id="d57c9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57c9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d57c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d57c9-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d57c9-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d57c9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d57c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d57c9-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d57c9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d57c9-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d57c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57c9-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57c9-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d57c9-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d57c9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d57c9-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d57c9-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d57c9-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d57c9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d57c9-136"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d57c9-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
