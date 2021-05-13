---
description: Copia un elemento o elementos en una carpeta.
title: Método Folder.CopyHere (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842146"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="5433c-103">Método Folder.CopyHere</span><span class="sxs-lookup"><span data-stu-id="5433c-103">Folder.CopyHere method</span></span>

<span data-ttu-id="5433c-104">Copia un elemento o elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5433c-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5433c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5433c-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="5433c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5433c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5433c-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="5433c-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="5433c-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5433c-108">Type: **Variant**</span></span>

<span data-ttu-id="5433c-109">Elemento o elementos que se copian.</span><span class="sxs-lookup"><span data-stu-id="5433c-109">The item or items to copy.</span></span> <span data-ttu-id="5433c-110">Puede ser una cadena que representa un nombre de archivo, un [**objeto FolderItem**](folderitem.md) o un [**objeto FolderItems.**](folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="5433c-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5433c-111">*vOptions* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="5433c-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5433c-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5433c-112">Type: **Variant**</span></span>

<span data-ttu-id="5433c-113">Opciones para la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="5433c-113">Options for the copy operation.</span></span> <span data-ttu-id="5433c-114">Este valor puede ser cero o una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5433c-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="5433c-115">Estos valores se basan en marcas definidas para su uso con el **miembro fFlags** de la estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) de C++.</span><span class="sxs-lookup"><span data-stu-id="5433c-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="5433c-116">Cada espacio de nombres de Shell debe proporcionar su propia implementación de estas marcas y cada espacio de nombres puede optar por omitir algunas o incluso todas estas marcas.</span><span class="sxs-lookup"><span data-stu-id="5433c-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="5433c-117">Estas marcas no se definen por nombre para Visual Basic, VBScript o JScript, por lo que debe definirlas usted mismo o usar sus equivalentes numéricos.</span><span class="sxs-lookup"><span data-stu-id="5433c-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="5433c-118">En algunos casos, como los archivos comprimidos (.zip), algunas marcas de opción pueden omitirse por diseño.</span><span class="sxs-lookup"><span data-stu-id="5433c-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="5433c-119">(4)</span><span class="sxs-lookup"><span data-stu-id="5433c-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-120">No mostrar un cuadro de diálogo de progreso.</span><span class="sxs-lookup"><span data-stu-id="5433c-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-121">(8)</span><span class="sxs-lookup"><span data-stu-id="5433c-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-122">Asigne al archivo que se está operando con un nombre nuevo en una operación de movimiento, copia o cambio de nombre si ya existe un archivo con el nombre de destino.</span><span class="sxs-lookup"><span data-stu-id="5433c-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-123">(16)</span><span class="sxs-lookup"><span data-stu-id="5433c-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-124">Responda con "Sí a todo" para cualquier cuadro de diálogo que se muestre.</span><span class="sxs-lookup"><span data-stu-id="5433c-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-125">(64)</span><span class="sxs-lookup"><span data-stu-id="5433c-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-126">Conserve la información de deshacer, si es posible.</span><span class="sxs-lookup"><span data-stu-id="5433c-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-127">(128)</span><span class="sxs-lookup"><span data-stu-id="5433c-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-128">Realice la operación en archivos solo si se especifica un nombre de archivo comodín ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="5433c-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-129">(256)</span><span class="sxs-lookup"><span data-stu-id="5433c-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-130">Mostrar un cuadro de diálogo de progreso, pero no mostrar los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="5433c-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-131">(512)</span><span class="sxs-lookup"><span data-stu-id="5433c-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-132">No confirme la creación de un nuevo directorio si la operación requiere que se cree uno.</span><span class="sxs-lookup"><span data-stu-id="5433c-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="5433c-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-134">No muestre una interfaz de usuario si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5433c-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="5433c-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="5433c-136">Versión 4.71.</span><span class="sxs-lookup"><span data-stu-id="5433c-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="5433c-137">No copie los atributos de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="5433c-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="5433c-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="5433c-139">Solo funciona en el directorio local.</span><span class="sxs-lookup"><span data-stu-id="5433c-139">Only operate in the local directory.</span></span> <span data-ttu-id="5433c-140">No funcione de forma recursiva en subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="5433c-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="5433c-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="5433c-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="5433c-142">Versión 5.0.</span><span class="sxs-lookup"><span data-stu-id="5433c-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="5433c-143">No copie los archivos conectados como un grupo.</span><span class="sxs-lookup"><span data-stu-id="5433c-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="5433c-144">Copie solo los archivos especificados.</span><span class="sxs-lookup"><span data-stu-id="5433c-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5433c-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5433c-145">Return value</span></span>

<span data-ttu-id="5433c-146">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5433c-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5433c-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5433c-147">Remarks</span></span>

<span data-ttu-id="5433c-148">No se envía ninguna notificación al programa que realiza la llamada para indicar que la copia se ha completado.</span><span class="sxs-lookup"><span data-stu-id="5433c-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="5433c-149">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="5433c-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="5433c-150">Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS).</span><span class="sxs-lookup"><span data-stu-id="5433c-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="5433c-151">Si intenta llamar a un método sin implementar, se 0x800A01BD error (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="5433c-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5433c-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5433c-152">Examples</span></span>

<span data-ttu-id="5433c-153">En el ejemplo siguiente se **usa CopyHere** para copiar el archivo Autoexec.bat desde el directorio raíz al directorio C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="5433c-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="5433c-154">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5433c-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5433c-155">Jscript:</span><span class="sxs-lookup"><span data-stu-id="5433c-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="5433c-156">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="5433c-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="5433c-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5433c-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5433c-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5433c-158">Requirements</span></span>



| <span data-ttu-id="5433c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5433c-159">Requirement</span></span> | <span data-ttu-id="5433c-160">Value</span><span class="sxs-lookup"><span data-stu-id="5433c-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5433c-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5433c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5433c-162">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="5433c-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5433c-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5433c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5433c-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5433c-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5433c-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5433c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="5433c-166"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5433c-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5433c-167">Idl</span><span class="sxs-lookup"><span data-stu-id="5433c-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5433c-168"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5433c-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5433c-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5433c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5433c-170"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5433c-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5433c-171">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5433c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5433c-172">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="5433c-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




