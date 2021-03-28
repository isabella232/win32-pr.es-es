---
description: Mueve un elemento o elementos a esta carpeta.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Método Folder. MoveHere (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808035"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="74bea-103">Folder. MoveHere (método)</span><span class="sxs-lookup"><span data-stu-id="74bea-103">Folder.MoveHere method</span></span>

<span data-ttu-id="74bea-104">Mueve un elemento o elementos a esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="74bea-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74bea-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="74bea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74bea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bea-107">*vItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74bea-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74bea-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="74bea-108">Type: **Variant**</span></span>

<span data-ttu-id="74bea-109">Elemento o elementos que se van a desplace.</span><span class="sxs-lookup"><span data-stu-id="74bea-109">The item or items to move.</span></span> <span data-ttu-id="74bea-110">Puede ser una cadena que representa un nombre de archivo, un objeto [**carpeta**](folderitem.md) o un objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="74bea-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="74bea-111">*vOptions* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="74bea-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74bea-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="74bea-112">Type: **Variant**</span></span>

<span data-ttu-id="74bea-113">Opciones de la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="74bea-113">Options for the move operation.</span></span> <span data-ttu-id="74bea-114">Este valor puede ser cero o una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="74bea-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="74bea-115">Estos valores se basan en marcas definidas para su uso con el miembro **fFlags** de la estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) de C++.</span><span class="sxs-lookup"><span data-stu-id="74bea-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="74bea-116">Estas marcas no se definen como tales para Visual Basic, VBScript o JScript, por lo que debe definirlas usted mismo o usar sus equivalentes numéricos.</span><span class="sxs-lookup"><span data-stu-id="74bea-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="74bea-117">(4)</span><span class="sxs-lookup"><span data-stu-id="74bea-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-118">No mostrar un cuadro de diálogo de progreso.</span><span class="sxs-lookup"><span data-stu-id="74bea-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-119">(8)</span><span class="sxs-lookup"><span data-stu-id="74bea-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-120">Dé al archivo que opere con un nuevo nombre en una operación de movimiento, copia o cambio de nombre si ya existe un archivo con el nombre de destino.</span><span class="sxs-lookup"><span data-stu-id="74bea-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-121">(16)</span><span class="sxs-lookup"><span data-stu-id="74bea-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-122">Responda con "sí a todo" para cualquier cuadro de diálogo que se muestre.</span><span class="sxs-lookup"><span data-stu-id="74bea-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-123">(64)</span><span class="sxs-lookup"><span data-stu-id="74bea-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-124">Si es posible, conserve la información de deshacer.</span><span class="sxs-lookup"><span data-stu-id="74bea-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-125">(128)</span><span class="sxs-lookup"><span data-stu-id="74bea-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-126">Realice la operación en archivos solo si se especifica un nombre de archivo comodín ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="74bea-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-127">(256)</span><span class="sxs-lookup"><span data-stu-id="74bea-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-128">Muestra un cuadro de diálogo de progreso pero no muestra los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="74bea-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-129">(512)</span><span class="sxs-lookup"><span data-stu-id="74bea-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-130">No confirme la creación de un directorio nuevo si la operación requiere que se cree uno.</span><span class="sxs-lookup"><span data-stu-id="74bea-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="74bea-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-132">No muestre una interfaz de usuario si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="74bea-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="74bea-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="74bea-134">Versión 4,71.</span><span class="sxs-lookup"><span data-stu-id="74bea-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="74bea-135">No copie los atributos de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="74bea-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="74bea-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="74bea-137">Solo funciona en el directorio local.</span><span class="sxs-lookup"><span data-stu-id="74bea-137">Only operate in the local directory.</span></span> <span data-ttu-id="74bea-138">No opere de forma recursiva en subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="74bea-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="74bea-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="74bea-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="74bea-140">Versión 5,0.</span><span class="sxs-lookup"><span data-stu-id="74bea-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="74bea-141">No mueva los archivos conectados como un grupo.</span><span class="sxs-lookup"><span data-stu-id="74bea-141">Do not move connected files as a group.</span></span> <span data-ttu-id="74bea-142">Solo mueve los archivos especificados.</span><span class="sxs-lookup"><span data-stu-id="74bea-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74bea-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74bea-143">Return value</span></span>

<span data-ttu-id="74bea-144">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="74bea-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74bea-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74bea-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74bea-146">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="74bea-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="74bea-147">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="74bea-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="74bea-148">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="74bea-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="74bea-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="74bea-149">Examples</span></span>

<span data-ttu-id="74bea-150">En el ejemplo siguiente se usa **MoveHere** para trasladar el archivo Temp.txt del directorio raíz de la unidad c a la \\ carpeta c: Windows.</span><span class="sxs-lookup"><span data-stu-id="74bea-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="74bea-151">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="74bea-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="74bea-152">JScript.net</span><span class="sxs-lookup"><span data-stu-id="74bea-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="74bea-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="74bea-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="74bea-154">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="74bea-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="74bea-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74bea-155">Requirements</span></span>



| <span data-ttu-id="74bea-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bea-156">Requirement</span></span> | <span data-ttu-id="74bea-157">Value</span><span class="sxs-lookup"><span data-stu-id="74bea-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74bea-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74bea-158">Minimum supported client</span></span><br/> | <span data-ttu-id="74bea-159">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="74bea-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74bea-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74bea-160">Minimum supported server</span></span><br/> | <span data-ttu-id="74bea-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74bea-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74bea-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74bea-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="74bea-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="74bea-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="74bea-164">IDL</span><span class="sxs-lookup"><span data-stu-id="74bea-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74bea-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74bea-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="74bea-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74bea-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74bea-167"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="74bea-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




