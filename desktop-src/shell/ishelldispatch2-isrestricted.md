---
description: Recupera el valor de restricción de un grupo del registro.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Método IShellDispatch2. IsRestricted (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984694"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="8d463-103">IShellDispatch2. IsRestricted, método</span><span class="sxs-lookup"><span data-stu-id="8d463-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="8d463-104">Recupera el valor de restricción de un grupo del registro.</span><span class="sxs-lookup"><span data-stu-id="8d463-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d463-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d463-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="8d463-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d463-107">*sGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d463-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d463-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="8d463-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="8d463-109">**Cadena** que contiene el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="8d463-109">A **String** that contains the group name.</span></span> <span data-ttu-id="8d463-110">Este valor es el nombre de una subclave del registro en la que se va a comprobar la restricción.</span><span class="sxs-lookup"><span data-stu-id="8d463-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="8d463-111">*sRestriction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d463-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d463-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="8d463-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="8d463-113">**Cadena** que contiene la restricción cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8d463-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d463-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d463-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8d463-115">JScript</span><span class="sxs-lookup"><span data-stu-id="8d463-115">JScript</span></span>

<span data-ttu-id="8d463-116">Type: \**Integer \** _</span><span class="sxs-lookup"><span data-stu-id="8d463-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="8d463-117">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="8d463-117">The value of the restriction.</span></span> <span data-ttu-id="8d463-118">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="8d463-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="8d463-119">VB</span><span class="sxs-lookup"><span data-stu-id="8d463-119">VB</span></span>

<span data-ttu-id="8d463-120">Tipo: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="8d463-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="8d463-121">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="8d463-121">The value of the restriction.</span></span> <span data-ttu-id="8d463-122">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="8d463-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d463-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d463-123">Remarks</span></span>

<span data-ttu-id="8d463-124">Este método se implementa y se obtiene acceso a él mediante el método [_ *Shell. IsRestricted* \*](./shell-isrestricted.md) .</span><span class="sxs-lookup"><span data-stu-id="8d463-124">This method is implemented and accessed through the [_ *Shell.IsRestricted*\*](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="8d463-125">**IsRestricted** busca primero un nombre de subclave que coincida con *sGroup* en la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="8d463-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="8d463-126">Las restricciones se declaran como valores de las subclaves de la Directiva individual.</span><span class="sxs-lookup"><span data-stu-id="8d463-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="8d463-127">Si la restricción denominada en *sRestriction* se encuentra en la subclave denominada en *sGroup*, **IsRestricted** devuelve el valor actual de la restricción.</span><span class="sxs-lookup"><span data-stu-id="8d463-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="8d463-128">Si no se encuentra la restricción en **HKEY \_ local \_ Machine**, se comprueba la misma subclave en **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="8d463-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="8d463-129">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8d463-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="8d463-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d463-130">Examples</span></span>

<span data-ttu-id="8d463-131">En los siguientes ejemplos se muestra el uso de **IsRestricted** para recuperar el valor de datos de la restricción **undockwithoutlogon** de la subclave **System** .</span><span class="sxs-lookup"><span data-stu-id="8d463-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="8d463-132">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="8d463-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="8d463-133">JScript.net</span><span class="sxs-lookup"><span data-stu-id="8d463-133">JScript:</span></span>


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



<span data-ttu-id="8d463-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="8d463-134">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8d463-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d463-135">Requirements</span></span>



| <span data-ttu-id="8d463-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d463-136">Requirement</span></span> | <span data-ttu-id="8d463-137">Value</span><span class="sxs-lookup"><span data-stu-id="8d463-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d463-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d463-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8d463-139">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8d463-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d463-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d463-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8d463-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d463-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8d463-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d463-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d463-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d463-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8d463-144">IDL</span><span class="sxs-lookup"><span data-stu-id="8d463-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d463-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d463-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8d463-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d463-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d463-147"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8d463-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
