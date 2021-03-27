---
description: Recupera los detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de la última modificación.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Método Folder. GetDetailsOf (ShlObj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000857"
---
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="bde8a-104">Folder. GetDetailsOf (método)</span><span class="sxs-lookup"><span data-stu-id="bde8a-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="bde8a-105">Recupera los detalles sobre un elemento de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="bde8a-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="bde8a-106">Por ejemplo, su tamaño, tipo o la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="bde8a-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde8a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bde8a-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="bde8a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bde8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde8a-109">*vItem*</span><span class="sxs-lookup"><span data-stu-id="bde8a-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="bde8a-110">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="bde8a-110">Type: **Variant**</span></span>

<span data-ttu-id="bde8a-111">Elemento para el que se va a recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="bde8a-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="bde8a-112">Debe ser un objeto [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="bde8a-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="bde8a-113">*iColumn*</span><span class="sxs-lookup"><span data-stu-id="bde8a-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="bde8a-114">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="bde8a-114">Type: **Integer**</span></span>

<span data-ttu-id="bde8a-115">Valor **entero** que especifica la información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bde8a-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="bde8a-116">La información disponible para un elemento depende de la carpeta en la que se muestra.</span><span class="sxs-lookup"><span data-stu-id="bde8a-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="bde8a-117">Este valor corresponde al número de columna de base cero que se muestra en una vista de Shell.</span><span class="sxs-lookup"><span data-stu-id="bde8a-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="bde8a-118">Para un elemento del sistema de archivos, puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="bde8a-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="bde8a-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="bde8a-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-120">Recupera el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="bde8a-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="bde8a-121">(1)</span><span class="sxs-lookup"><span data-stu-id="bde8a-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-122">Recupera el tamaño del elemento.</span><span class="sxs-lookup"><span data-stu-id="bde8a-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="bde8a-123">(2)</span><span class="sxs-lookup"><span data-stu-id="bde8a-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-124">Recupera el tipo del elemento.</span><span class="sxs-lookup"><span data-stu-id="bde8a-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="bde8a-125">(3)</span><span class="sxs-lookup"><span data-stu-id="bde8a-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-126">Recupera la fecha y la hora en que se modificó el elemento por última vez.</span><span class="sxs-lookup"><span data-stu-id="bde8a-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="bde8a-127">(4)</span><span class="sxs-lookup"><span data-stu-id="bde8a-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-128">Recupera los atributos del elemento.</span><span class="sxs-lookup"><span data-stu-id="bde8a-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="bde8a-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="bde8a-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="bde8a-130">Recupera la información de información sobre herramientas para el elemento.</span><span class="sxs-lookup"><span data-stu-id="bde8a-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde8a-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bde8a-131">Return value</span></span>

<span data-ttu-id="bde8a-132">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="bde8a-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="bde8a-133">Cadena que contiene los detalles recuperados.</span><span class="sxs-lookup"><span data-stu-id="bde8a-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="bde8a-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bde8a-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bde8a-135">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="bde8a-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="bde8a-136">Por ejemplo, el método [_ *ParseName* \*](folder-parsename.md) no está implementado para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="bde8a-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="bde8a-137">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="bde8a-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bde8a-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bde8a-138">Examples</span></span>

<span data-ttu-id="bde8a-139">En el ejemplo siguiente se usa **GetDetailsOf** para recuperar el tipo del archivo denominado Clock.avi.</span><span class="sxs-lookup"><span data-stu-id="bde8a-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="bde8a-140">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bde8a-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bde8a-141">JScript.net</span><span class="sxs-lookup"><span data-stu-id="bde8a-141">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



<span data-ttu-id="bde8a-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="bde8a-142">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="bde8a-143">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bde8a-143">Visual Basic:</span></span>


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bde8a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bde8a-144">Requirements</span></span>



| <span data-ttu-id="bde8a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde8a-145">Requirement</span></span> | <span data-ttu-id="bde8a-146">Value</span><span class="sxs-lookup"><span data-stu-id="bde8a-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde8a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bde8a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bde8a-148">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bde8a-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bde8a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bde8a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bde8a-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bde8a-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bde8a-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bde8a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde8a-152"><dt>ShlObj \_ Core. h (incluye Shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bde8a-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="bde8a-153">IDL</span><span class="sxs-lookup"><span data-stu-id="bde8a-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bde8a-154"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bde8a-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bde8a-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bde8a-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bde8a-156"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bde8a-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
