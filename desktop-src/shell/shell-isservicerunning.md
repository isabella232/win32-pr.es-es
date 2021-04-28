---
description: 'Método Shell.IsServiceRunning: devuelve un valor que indica si se está ejecutando un servicio determinado.'
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Método Shell.IsServiceRunning (Shldisp.h)
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
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083729"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="74ab5-103">Método Shell.IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="74ab5-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="74ab5-104">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="74ab5-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ab5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74ab5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="74ab5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ab5-107">*sServiceName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="74ab5-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ab5-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="74ab5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="74ab5-109">Cadena **que** contiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="74ab5-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ab5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74ab5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="74ab5-111">JScript</span><span class="sxs-lookup"><span data-stu-id="74ab5-111">JScript</span></span>

<span data-ttu-id="74ab5-112">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="74ab5-112">Type: **Variant\***</span></span>

<span data-ttu-id="74ab5-113">Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="74ab5-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="74ab5-114">VB</span><span class="sxs-lookup"><span data-stu-id="74ab5-114">VB</span></span>

<span data-ttu-id="74ab5-115">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="74ab5-115">Type: **Variant\***</span></span>

<span data-ttu-id="74ab5-116">Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="74ab5-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="74ab5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74ab5-117">Remarks</span></span>

<span data-ttu-id="74ab5-118">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="74ab5-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="74ab5-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="74ab5-119">Examples</span></span>

<span data-ttu-id="74ab5-120">En los ejemplos siguientes se muestra el uso de **IsServiceRunning para** determinar si el servicio Themes se está ejecutando para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74ab5-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="74ab5-121">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="74ab5-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="74ab5-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="74ab5-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="74ab5-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="74ab5-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="74ab5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ab5-124">Requirements</span></span>



| <span data-ttu-id="74ab5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ab5-125">Requirement</span></span> | <span data-ttu-id="74ab5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ab5-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ab5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="74ab5-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="74ab5-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74ab5-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ab5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="74ab5-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74ab5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="74ab5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74ab5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ab5-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="74ab5-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="74ab5-133">Idl</span><span class="sxs-lookup"><span data-stu-id="74ab5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74ab5-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="74ab5-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="74ab5-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74ab5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ab5-136"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="74ab5-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
