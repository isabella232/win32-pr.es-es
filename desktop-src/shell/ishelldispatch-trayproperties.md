---
description: Muestra el cuadro de diálogo Propiedades de la barra de tareas y del menú Inicio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Propiedades.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Método IShellDispatch. TrayProperties (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001342"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="c5c7b-104">IShellDispatch. TrayProperties, método</span><span class="sxs-lookup"><span data-stu-id="c5c7b-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="c5c7b-105">Muestra el cuadro de diálogo Propiedades de la **barra de tareas y del menú Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="c5c7b-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c7b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5c7b-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="c5c7b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5c7b-108">Parameters</span></span>

<span data-ttu-id="c5c7b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5c7b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5c7b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c5c7b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c5c7b-111">JScript</span></span>

<span data-ttu-id="c5c7b-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c5c7b-113">VB</span><span class="sxs-lookup"><span data-stu-id="c5c7b-113">VB</span></span>

<span data-ttu-id="c5c7b-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c7b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5c7b-115">Remarks</span></span>

<span data-ttu-id="c5c7b-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c5c7b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c5c7b-117">Examples</span></span>

<span data-ttu-id="c5c7b-118">En los siguientes ejemplos se muestra el uso de **TrayProperties** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c5c7b-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="c5c7b-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="c5c7b-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="c5c7b-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c5c7b-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c5c7b-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c5c7b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5c7b-122">Requirements</span></span>



| <span data-ttu-id="c5c7b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c7b-123">Requirement</span></span> | <span data-ttu-id="c5c7b-124">Value</span><span class="sxs-lookup"><span data-stu-id="c5c7b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c7b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c7b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c7b-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c5c7b-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5c7b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c7b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c7b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5c7b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5c7b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5c7b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c7b-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c7b-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c5c7b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="c5c7b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5c7b-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5c7b-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c5c7b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5c7b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c7b-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c5c7b-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




