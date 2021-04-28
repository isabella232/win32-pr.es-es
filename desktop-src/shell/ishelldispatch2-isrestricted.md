---
description: 'Método IShellDispatch2.IsRestricted: recupera la configuración de restricción de un grupo del Registro.'
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Método IShellDispatch2.IsRestricted (Shldisp.h)
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
ms.openlocfilehash: b4f482407fadd16d7ecfe9deeafd91b032a9a24f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117103"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="a9631-103">Método IShellDispatch2.IsRestricted</span><span class="sxs-lookup"><span data-stu-id="a9631-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="a9631-104">Recupera la configuración de restricción de un grupo del Registro.</span><span class="sxs-lookup"><span data-stu-id="a9631-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9631-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9631-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a9631-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9631-107">*sGroup* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a9631-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9631-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a9631-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a9631-109">Cadena **que** contiene el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="a9631-109">A **String** that contains the group name.</span></span> <span data-ttu-id="a9631-110">Este valor es el nombre de una subclave del Registro con la que se va a comprobar la restricción.</span><span class="sxs-lookup"><span data-stu-id="a9631-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="a9631-111">*sRestriction* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a9631-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9631-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a9631-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a9631-113">Cadena **que** contiene la restricción cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a9631-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9631-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9631-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a9631-115">JScript</span><span class="sxs-lookup"><span data-stu-id="a9631-115">JScript</span></span>

<span data-ttu-id="a9631-116">Tipo: **\* Entero**</span><span class="sxs-lookup"><span data-stu-id="a9631-116">Type: **Integer\***</span></span>

<span data-ttu-id="a9631-117">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="a9631-117">The value of the restriction.</span></span> <span data-ttu-id="a9631-118">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="a9631-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="a9631-119">VB</span><span class="sxs-lookup"><span data-stu-id="a9631-119">VB</span></span>

<span data-ttu-id="a9631-120">Tipo: **\* Entero**</span><span class="sxs-lookup"><span data-stu-id="a9631-120">Type: **Integer\***</span></span>

<span data-ttu-id="a9631-121">Valor de la restricción.</span><span class="sxs-lookup"><span data-stu-id="a9631-121">The value of the restriction.</span></span> <span data-ttu-id="a9631-122">Si no se encuentra la restricción especificada, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="a9631-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9631-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9631-123">Remarks</span></span>

<span data-ttu-id="a9631-124">Este método se implementa y se accede a través del [**método Shell.IsRestricted.**](./shell-isrestricted.md)</span><span class="sxs-lookup"><span data-stu-id="a9631-124">This method is implemented and accessed through the [**Shell.IsRestricted**](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="a9631-125">**IsRestricted** busca primero un nombre de subclave que coincida *con sGroup* bajo la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="a9631-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="a9631-126">Las restricciones se declaran como valores de las subclaves de directiva individuales.</span><span class="sxs-lookup"><span data-stu-id="a9631-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="a9631-127">Si la restricción denominada en *sRestriction* se encuentra en la subclave denominada *en sGroup*, **IsRestricted** devuelve el valor actual de la restricción.</span><span class="sxs-lookup"><span data-stu-id="a9631-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="a9631-128">Si la restricción no se encuentra en **HKEY \_ LOCAL \_ MACHINE**, la misma subclave se comprueba en **HKEY \_ CURRENT \_ USER**.</span><span class="sxs-lookup"><span data-stu-id="a9631-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="a9631-129">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a9631-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a9631-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a9631-130">Examples</span></span>

<span data-ttu-id="a9631-131">En los ejemplos siguientes se muestra el uso de **IsRestricted** para recuperar el valor de datos de la restricción **undockwithoutlogon** de la subclave **System.**</span><span class="sxs-lookup"><span data-stu-id="a9631-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="a9631-132">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="a9631-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="a9631-133">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a9631-133">JScript:</span></span>


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



<span data-ttu-id="a9631-134">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a9631-134">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a9631-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9631-135">Requirements</span></span>



| <span data-ttu-id="a9631-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9631-136">Requirement</span></span> | <span data-ttu-id="a9631-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a9631-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9631-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9631-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a9631-139">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="a9631-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9631-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9631-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a9631-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9631-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a9631-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9631-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9631-143"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a9631-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a9631-144">Idl</span><span class="sxs-lookup"><span data-stu-id="a9631-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9631-145"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9631-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a9631-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9631-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9631-147"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a9631-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
