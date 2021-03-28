---
description: Muestra el cuadro de diálogo Buscar impresora.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Método Shell. FindPrinter (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985978"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="66224-103">Shell. FindPrinter (método)</span><span class="sxs-lookup"><span data-stu-id="66224-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="66224-104">Muestra el cuadro de diálogo **Buscar impresora** .</span><span class="sxs-lookup"><span data-stu-id="66224-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="66224-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66224-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="66224-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66224-107">*sName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66224-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66224-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="66224-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="66224-109">**Cadena** que contiene el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="66224-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="66224-110">*sLocation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66224-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66224-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="66224-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="66224-112">**Cadena** que contiene la ubicación de la impresora.</span><span class="sxs-lookup"><span data-stu-id="66224-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="66224-113">*sModel* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66224-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66224-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="66224-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="66224-115">**Cadena** que contiene el modelo de impresora.</span><span class="sxs-lookup"><span data-stu-id="66224-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66224-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66224-116">Remarks</span></span>

<span data-ttu-id="66224-117">Si asigna cadenas a uno o varios parámetros opcionales, se muestran como valores predeterminados en el control de edición asociado cuando se muestra el cuadro de diálogo **Buscar impresora** .</span><span class="sxs-lookup"><span data-stu-id="66224-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="66224-118">El usuario puede aceptar o invalidar estos valores.</span><span class="sxs-lookup"><span data-stu-id="66224-118">The user can either accept or override these values.</span></span> <span data-ttu-id="66224-119">Si no se asigna ningún valor a un parámetro, el cuadro de edición asociado está vacío y el usuario debe escribir un valor.</span><span class="sxs-lookup"><span data-stu-id="66224-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="66224-120">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="66224-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="66224-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="66224-121">Examples</span></span>

<span data-ttu-id="66224-122">En los siguientes ejemplos se muestra el uso de **FindPrinter** para mostrar el cuadro de diálogo **Buscar impresora** para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="66224-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="66224-123">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="66224-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="66224-124">JScript.net</span><span class="sxs-lookup"><span data-stu-id="66224-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="66224-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="66224-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="66224-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66224-126">Requirements</span></span>



| <span data-ttu-id="66224-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66224-127">Requirement</span></span> | <span data-ttu-id="66224-128">Value</span><span class="sxs-lookup"><span data-stu-id="66224-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66224-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66224-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66224-130">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="66224-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66224-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66224-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66224-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="66224-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="66224-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66224-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="66224-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="66224-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="66224-135">IDL</span><span class="sxs-lookup"><span data-stu-id="66224-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66224-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66224-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="66224-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66224-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66224-138"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="66224-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
