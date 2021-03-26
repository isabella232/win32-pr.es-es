---
description: Muestra el cuadro de diálogo Propiedades de la barra de tareas y del menú Inicio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Propiedades.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Método Shell. TrayProperties (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985962"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="c5158-104">Shell. TrayProperties (método)</span><span class="sxs-lookup"><span data-stu-id="c5158-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="c5158-105">Muestra el cuadro de diálogo Propiedades de la **barra de tareas y del menú Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c5158-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="c5158-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="c5158-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5158-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5158-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="c5158-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5158-108">Parameters</span></span>

<span data-ttu-id="c5158-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5158-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c5158-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c5158-110">Examples</span></span>

<span data-ttu-id="c5158-111">En el ejemplo siguiente se muestra **TrayProperties** en uso.</span><span class="sxs-lookup"><span data-stu-id="c5158-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="c5158-112">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c5158-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c5158-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="c5158-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="c5158-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="c5158-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c5158-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c5158-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c5158-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5158-116">Requirements</span></span>



| <span data-ttu-id="c5158-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5158-117">Requirement</span></span> | <span data-ttu-id="c5158-118">Value</span><span class="sxs-lookup"><span data-stu-id="c5158-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5158-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5158-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5158-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c5158-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5158-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5158-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5158-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5158-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5158-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5158-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5158-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c5158-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c5158-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5158-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c5158-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5158-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5158-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




