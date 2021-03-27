---
description: Crea una nueva carpeta.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Folder. NuevaCarpeta (método) (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001913"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="42bde-103">Folder. NuevaCarpeta (método)</span><span class="sxs-lookup"><span data-stu-id="42bde-103">Folder.NewFolder method</span></span>

<span data-ttu-id="42bde-104">Crea una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="42bde-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="42bde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42bde-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="42bde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42bde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42bde-107">*bName*</span><span class="sxs-lookup"><span data-stu-id="42bde-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="42bde-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="42bde-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="42bde-109">Cadena que especifica el nombre de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="42bde-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="42bde-110">*vOptions* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="42bde-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42bde-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="42bde-111">Type: **Variant**</span></span>

<span data-ttu-id="42bde-112">Este valor no se utiliza actualmente.</span><span class="sxs-lookup"><span data-stu-id="42bde-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42bde-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42bde-113">Return value</span></span>

<span data-ttu-id="42bde-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="42bde-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42bde-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42bde-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42bde-116">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="42bde-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="42bde-117">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="42bde-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="42bde-118">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="42bde-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="42bde-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="42bde-119">Examples</span></span>

<span data-ttu-id="42bde-120">En el ejemplo siguiente se usa **NuevaCarpeta** para crear la nueva carpeta C: \\ TestFolder.</span><span class="sxs-lookup"><span data-stu-id="42bde-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="42bde-121">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="42bde-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="42bde-122">JScript.net</span><span class="sxs-lookup"><span data-stu-id="42bde-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="42bde-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="42bde-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="42bde-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="42bde-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="42bde-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42bde-125">Requirements</span></span>



| <span data-ttu-id="42bde-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42bde-126">Requirement</span></span> | <span data-ttu-id="42bde-127">Value</span><span class="sxs-lookup"><span data-stu-id="42bde-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bde-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42bde-128">Minimum supported client</span></span><br/> | <span data-ttu-id="42bde-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="42bde-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42bde-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42bde-130">Minimum supported server</span></span><br/> | <span data-ttu-id="42bde-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42bde-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42bde-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42bde-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="42bde-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42bde-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42bde-134">IDL</span><span class="sxs-lookup"><span data-stu-id="42bde-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42bde-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42bde-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42bde-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42bde-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42bde-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="42bde-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
