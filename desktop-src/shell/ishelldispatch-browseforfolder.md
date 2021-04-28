---
description: 'Método IShellDispatch.BrowseForFolder: crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de la carpeta seleccionada.'
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Método IShellDispatch.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086693"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="413c8-103">Método IShellDispatch.BrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="413c8-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="413c8-104">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Carpeta de [**la carpeta**](folder.md) seleccionada.</span><span class="sxs-lookup"><span data-stu-id="413c8-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="413c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="413c8-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="413c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="413c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413c8-107">*Hwnd* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="413c8-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413c8-108">Tipo: **Entero**</span><span class="sxs-lookup"><span data-stu-id="413c8-108">Type: **Integer**</span></span>

<span data-ttu-id="413c8-109">Identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="413c8-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="413c8-110">Este valor puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="413c8-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="413c8-111">*sTitle* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="413c8-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413c8-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="413c8-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="413c8-113">Valor **string** que representa el título que se muestra dentro del **cuadro de** diálogo Examinar.</span><span class="sxs-lookup"><span data-stu-id="413c8-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="413c8-114">*iOptions* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="413c8-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413c8-115">Tipo: **Entero**</span><span class="sxs-lookup"><span data-stu-id="413c8-115">Type: **Integer**</span></span>

<span data-ttu-id="413c8-116">Valor **entero** que contiene las opciones para el método .</span><span class="sxs-lookup"><span data-stu-id="413c8-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="413c8-117">Puede ser cero o una combinación de los valores enumerados en el **miembro ulFlags** de la [**estructura BROWSEINFO.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)</span><span class="sxs-lookup"><span data-stu-id="413c8-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="413c8-118">*vRootFolder* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="413c8-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="413c8-119">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="413c8-119">Type: **Variant**</span></span>

<span data-ttu-id="413c8-120">Carpeta raíz que se usará en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="413c8-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="413c8-121">El usuario no puede examinar más arriba en el árbol que esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="413c8-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="413c8-122">Si no se especifica este valor, la carpeta raíz que se usa en el cuadro de diálogo es el escritorio.</span><span class="sxs-lookup"><span data-stu-id="413c8-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="413c8-123">Este valor puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="413c8-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="413c8-124">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="413c8-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="413c8-125">En esos casos, los valores numéricos deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="413c8-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413c8-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="413c8-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="413c8-127">JScript</span><span class="sxs-lookup"><span data-stu-id="413c8-127">JScript</span></span>

<span data-ttu-id="413c8-128">Tipo: **\* \* FOLDER**</span><span class="sxs-lookup"><span data-stu-id="413c8-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="413c8-129">Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.</span><span class="sxs-lookup"><span data-stu-id="413c8-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="413c8-130">VB</span><span class="sxs-lookup"><span data-stu-id="413c8-130">VB</span></span>

<span data-ttu-id="413c8-131">Tipo: **\* \* FOLDER**</span><span class="sxs-lookup"><span data-stu-id="413c8-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="413c8-132">Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.</span><span class="sxs-lookup"><span data-stu-id="413c8-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="413c8-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="413c8-133">Remarks</span></span>

<span data-ttu-id="413c8-134">Este método se implementa y se accede a través del [**método Shell.BrowseForFolder.**](shell-browseforfolder.md)</span><span class="sxs-lookup"><span data-stu-id="413c8-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="413c8-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="413c8-135">Examples</span></span>

<span data-ttu-id="413c8-136">En los ejemplos siguientes se **usa BrowseForFolder para** mostrar una ventana de exploración titulada "Example" rooteado en la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="413c8-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="413c8-137">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="413c8-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="413c8-138">Jscript:</span><span class="sxs-lookup"><span data-stu-id="413c8-138">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="413c8-139">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="413c8-139">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="413c8-140">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="413c8-140">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="413c8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="413c8-141">Requirements</span></span>



| <span data-ttu-id="413c8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="413c8-142">Requirement</span></span> | <span data-ttu-id="413c8-143">Valor</span><span class="sxs-lookup"><span data-stu-id="413c8-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="413c8-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="413c8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="413c8-145">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="413c8-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="413c8-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="413c8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="413c8-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="413c8-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="413c8-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="413c8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="413c8-149"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="413c8-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="413c8-150">Idl</span><span class="sxs-lookup"><span data-stu-id="413c8-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="413c8-151"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="413c8-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="413c8-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="413c8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="413c8-153"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="413c8-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
