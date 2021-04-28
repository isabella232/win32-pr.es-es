---
description: 'Método IShellDispatch2.FindPrinter: muestra el cuadro de diálogo Buscar impresora.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Método IShellDispatch2.FindPrinter (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117123"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="28e4e-103">Método IShellDispatch2.FindPrinter</span><span class="sxs-lookup"><span data-stu-id="28e4e-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="28e4e-104">Muestra el **cuadro de diálogo Buscar** impresora.</span><span class="sxs-lookup"><span data-stu-id="28e4e-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e4e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e4e-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="28e4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28e4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e4e-107">*sName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28e4e-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28e4e-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="28e4e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="28e4e-109">Cadena **que** contiene el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="28e4e-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="28e4e-110">*sLocation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28e4e-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28e4e-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="28e4e-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="28e4e-112">Cadena **que** contiene la ubicación de la impresora.</span><span class="sxs-lookup"><span data-stu-id="28e4e-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="28e4e-113">*sModel* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28e4e-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28e4e-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="28e4e-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="28e4e-115">Cadena **que** contiene el modelo de impresora.</span><span class="sxs-lookup"><span data-stu-id="28e4e-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28e4e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28e4e-116">Remarks</span></span>

<span data-ttu-id="28e4e-117">Este método se implementa y se accede a este método a través [**del método Shell.FindPrinter.**](./shell-findprinter.md)</span><span class="sxs-lookup"><span data-stu-id="28e4e-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="28e4e-118">Si asigna cadenas a uno o varios de los parámetros opcionales, se muestran  como valores predeterminados en el control de edición asociado cuando se muestra el cuadro de diálogo Buscar impresora.</span><span class="sxs-lookup"><span data-stu-id="28e4e-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="28e4e-119">El usuario puede aceptar o invalidar estos valores.</span><span class="sxs-lookup"><span data-stu-id="28e4e-119">The user can either accept or override these values.</span></span> <span data-ttu-id="28e4e-120">Si no se asigna ningún valor a un parámetro, el cuadro de edición asociado está vacío y el usuario debe escribir un valor.</span><span class="sxs-lookup"><span data-stu-id="28e4e-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="28e4e-121">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="28e4e-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="28e4e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="28e4e-122">Examples</span></span>

<span data-ttu-id="28e4e-123">En los ejemplos siguientes se muestra el uso **de FindPrinter para** mostrar el cuadro de **diálogo** Buscar impresora de una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="28e4e-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="28e4e-124">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="28e4e-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="28e4e-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="28e4e-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="28e4e-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="28e4e-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="28e4e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e4e-127">Requirements</span></span>



| <span data-ttu-id="28e4e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e4e-128">Requirement</span></span> | <span data-ttu-id="28e4e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="28e4e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e4e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e4e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28e4e-131">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="28e4e-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28e4e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e4e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28e4e-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28e4e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="28e4e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28e4e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e4e-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="28e4e-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="28e4e-136">Idl</span><span class="sxs-lookup"><span data-stu-id="28e4e-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28e4e-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="28e4e-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="28e4e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28e4e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28e4e-139"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="28e4e-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
