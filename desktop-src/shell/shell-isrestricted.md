---
description: Recupera el valor de restricción de un grupo del registro.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Método Shell. IsRestricted (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277409"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="e76a4-103">Shell. IsRestricted (método)</span><span class="sxs-lookup"><span data-stu-id="e76a4-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="e76a4-104">Recupera el valor de restricción de un grupo del registro.</span><span class="sxs-lookup"><span data-stu-id="e76a4-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e76a4-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="e76a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e76a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76a4-107">*sGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e76a4-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76a4-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e76a4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e76a4-109">**Cadena** que contiene el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="e76a4-109">A **String** that contains the group name.</span></span> <span data-ttu-id="e76a4-110">Este valor es el nombre de una subclave del registro en la que se va a comprobar la restricción.</span><span class="sxs-lookup"><span data-stu-id="e76a4-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="e76a4-111">*sRestriction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e76a4-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76a4-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e76a4-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e76a4-113">**Cadena** que contiene la restricción cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e76a4-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76a4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e76a4-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e76a4-115">JScript</span><span class="sxs-lookup"><span data-stu-id="e76a4-115">JScript</span></span>

<span data-ttu-id="e76a4-116">Type: \**Integer \** _</span><span class="sxs-lookup"><span data-stu-id="e76a4-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="e76a4-117">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="e76a4-117">The value of the restriction.</span></span> <span data-ttu-id="e76a4-118">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="e76a4-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="e76a4-119">VB</span><span class="sxs-lookup"><span data-stu-id="e76a4-119">VB</span></span>

<span data-ttu-id="e76a4-120">Tipo: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="e76a4-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="e76a4-121">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="e76a4-121">The value of the restriction.</span></span> <span data-ttu-id="e76a4-122">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="e76a4-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76a4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e76a4-123">Remarks</span></span>

<span data-ttu-id="e76a4-124">_ *IsRestricted*\* busca primero un nombre de subclave que coincida con *sGroup* en la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="e76a4-124">_ *IsRestricted*\* first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="e76a4-125">Las restricciones se declaran como valores de las subclaves de la Directiva individual.</span><span class="sxs-lookup"><span data-stu-id="e76a4-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="e76a4-126">Si la restricción denominada en *sRestriction* se encuentra en la subclave denominada en *sGroup*, **IsRestricted** devuelve el valor actual de la restricción.</span><span class="sxs-lookup"><span data-stu-id="e76a4-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="e76a4-127">Si no se encuentra la restricción en **HKEY \_ local \_ Machine**, se comprueba la misma subclave en **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="e76a4-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="e76a4-128">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e76a4-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="e76a4-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e76a4-129">Examples</span></span>

<span data-ttu-id="e76a4-130">En los siguientes ejemplos se muestra el uso de **IsRestricted** para recuperar el valor de datos de la restricción **undockwithoutlogon** de la subclave **System** .</span><span class="sxs-lookup"><span data-stu-id="e76a4-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="e76a4-131">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="e76a4-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="e76a4-132">JScript.net</span><span class="sxs-lookup"><span data-stu-id="e76a4-132">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="e76a4-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="e76a4-133">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="e76a4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76a4-134">Requirements</span></span>



| <span data-ttu-id="e76a4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76a4-135">Requirement</span></span> | <span data-ttu-id="e76a4-136">Value</span><span class="sxs-lookup"><span data-stu-id="e76a4-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76a4-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76a4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e76a4-138">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e76a4-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e76a4-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76a4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e76a4-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e76a4-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e76a4-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e76a4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76a4-142"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76a4-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e76a4-143">IDL</span><span class="sxs-lookup"><span data-stu-id="e76a4-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e76a4-144"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e76a4-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e76a4-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e76a4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e76a4-146"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e76a4-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
