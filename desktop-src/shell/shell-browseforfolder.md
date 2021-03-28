---
description: Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de carpeta de la carpeta seleccionada.
title: Método Shell. BrowseForFolder (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082894"
---
# <a name="shellbrowseforfolder-method"></a><span data-ttu-id="f91ce-103">Shell. BrowseForFolder (método)</span><span class="sxs-lookup"><span data-stu-id="f91ce-103">Shell.BrowseForFolder method</span></span>

<span data-ttu-id="f91ce-104">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de [**carpeta**](folder.md) de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f91ce-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f91ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f91ce-105">Syntax</span></span>


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="f91ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f91ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f91ce-107">*HWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f91ce-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f91ce-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="f91ce-108">Type: **Integer**</span></span>

<span data-ttu-id="f91ce-109">Identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f91ce-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="f91ce-110">Este valor puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="f91ce-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f91ce-111">*sTitle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f91ce-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f91ce-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f91ce-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f91ce-113">Valor de **cadena** que representa el título que se muestra en el cuadro de diálogo **examinar** .</span><span class="sxs-lookup"><span data-stu-id="f91ce-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f91ce-114">*iOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f91ce-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f91ce-115">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="f91ce-115">Type: **Integer**</span></span>

<span data-ttu-id="f91ce-116">Valor **entero** que contiene las opciones para el método.</span><span class="sxs-lookup"><span data-stu-id="f91ce-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="f91ce-117">Puede ser cero o una combinación de los valores enumerados en el miembro **ulFlags** de la estructura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f91ce-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f91ce-118">*vRootFolder* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f91ce-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f91ce-119">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f91ce-119">Type: **Variant**</span></span>

<span data-ttu-id="f91ce-120">Carpeta raíz que se va a utilizar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f91ce-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="f91ce-121">El usuario no puede examinar más arriba en el árbol que esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="f91ce-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="f91ce-122">Si no se especifica este valor, la carpeta raíz usada en el cuadro de diálogo es el escritorio.</span><span class="sxs-lookup"><span data-stu-id="f91ce-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="f91ce-123">Este valor puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="f91ce-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="f91ce-124">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="f91ce-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="f91ce-125">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f91ce-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f91ce-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f91ce-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f91ce-127">JScript</span><span class="sxs-lookup"><span data-stu-id="f91ce-127">JScript</span></span>

<span data-ttu-id="f91ce-128">Tipo: **carpeta \* \***</span><span class="sxs-lookup"><span data-stu-id="f91ce-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="f91ce-129">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f91ce-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="f91ce-130">VB</span><span class="sxs-lookup"><span data-stu-id="f91ce-130">VB</span></span>

<span data-ttu-id="f91ce-131">Tipo: **carpeta \* \***</span><span class="sxs-lookup"><span data-stu-id="f91ce-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="f91ce-132">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f91ce-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="f91ce-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f91ce-133">Examples</span></span>

<span data-ttu-id="f91ce-134">En el ejemplo siguiente se usa **BrowseForFolder** para mostrar una ventana de exploración titulada "example" con la raíz de la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="f91ce-134">The following example uses **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="f91ce-135">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f91ce-135">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f91ce-136">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f91ce-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="f91ce-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="f91ce-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f91ce-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f91ce-138">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f91ce-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f91ce-139">Requirements</span></span>



| <span data-ttu-id="f91ce-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f91ce-140">Requirement</span></span> | <span data-ttu-id="f91ce-141">Value</span><span class="sxs-lookup"><span data-stu-id="f91ce-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f91ce-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f91ce-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f91ce-143">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f91ce-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f91ce-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f91ce-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f91ce-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f91ce-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f91ce-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f91ce-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f91ce-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f91ce-147"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f91ce-148">IDL</span><span class="sxs-lookup"><span data-stu-id="f91ce-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f91ce-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f91ce-149"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f91ce-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f91ce-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f91ce-151"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f91ce-151"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
