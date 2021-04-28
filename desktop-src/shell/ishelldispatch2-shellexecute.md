---
description: 'Método IShellDispatch2.ShellExecute: realiza una operación especificada en un archivo especificado.'
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Método IShellDispatch2.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117023"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="457c3-103">Método IShellDispatch2.ShellExecute</span><span class="sxs-lookup"><span data-stu-id="457c3-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="457c3-104">Realiza una operación especificada en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="457c3-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="457c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="457c3-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="457c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="457c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457c3-107">*sFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="457c3-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="457c3-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="457c3-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="457c3-109">Cadena **que** contiene el nombre del archivo en el que **ShellExecute** realizará la acción especificada por *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="457c3-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="457c3-110">*vArguments* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="457c3-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="457c3-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="457c3-111">Type: **Variant**</span></span>

<span data-ttu-id="457c3-112">Cadena que contiene valores de parámetro para la operación.</span><span class="sxs-lookup"><span data-stu-id="457c3-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="457c3-113">*vDirectory* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="457c3-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="457c3-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="457c3-114">Type: **Variant**</span></span>

<span data-ttu-id="457c3-115">Ruta de acceso completa del directorio que contiene el archivo especificado por *sFile*.</span><span class="sxs-lookup"><span data-stu-id="457c3-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="457c3-116">Si no se especifica este parámetro, se usa el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="457c3-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="457c3-117">*vOperation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="457c3-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="457c3-118">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="457c3-118">Type: **Variant**</span></span>

<span data-ttu-id="457c3-119">La operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="457c3-119">The operation to be performed.</span></span> <span data-ttu-id="457c3-120">Este valor se establece en una de las cadenas de verbo admitidas por el archivo .</span><span class="sxs-lookup"><span data-stu-id="457c3-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="457c3-121">Para obtener una explicación de los verbos, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="457c3-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="457c3-122">Si no se especifica este parámetro, se realiza la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="457c3-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="457c3-123">*vShow* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="457c3-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="457c3-124">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="457c3-124">Type: **Variant**</span></span>

<span data-ttu-id="457c3-125">Una recomendación sobre cómo se debe mostrar inicialmente la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="457c3-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="457c3-126">La aplicación puede omitir esta recomendación.</span><span class="sxs-lookup"><span data-stu-id="457c3-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="457c3-127">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="457c3-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="457c3-128">Si no se especifica este parámetro, la aplicación usa su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="457c3-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="457c3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="457c3-129">Value</span></span>                                                                                                                               | <span data-ttu-id="457c3-130">Significado</span><span class="sxs-lookup"><span data-stu-id="457c3-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="457c3-131"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="457c3-132">Abra la aplicación con una ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="457c3-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="457c3-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="457c3-134">Abra la aplicación con una ventana normal.</span><span class="sxs-lookup"><span data-stu-id="457c3-134">Open the application with a normal window.</span></span> <span data-ttu-id="457c3-135">Si la ventana se minimiza o maximiza, el sistema la restaura a su tamaño y posición originales.</span><span class="sxs-lookup"><span data-stu-id="457c3-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="457c3-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="457c3-137">Abra la aplicación con una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="457c3-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="457c3-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="457c3-139">Abra la aplicación con una ventana maximizada.</span><span class="sxs-lookup"><span data-stu-id="457c3-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="457c3-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="457c3-141">Abra la aplicación con su ventana en su tamaño y posición más recientes.</span><span class="sxs-lookup"><span data-stu-id="457c3-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="457c3-142">La ventana activa permanece activa.</span><span class="sxs-lookup"><span data-stu-id="457c3-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="457c3-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="457c3-144">Abra la aplicación con su ventana en su tamaño y posición actuales.</span><span class="sxs-lookup"><span data-stu-id="457c3-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="457c3-145"><dt></dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="457c3-146">Abra la aplicación con una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="457c3-146">Open the application with a minimized window.</span></span> <span data-ttu-id="457c3-147">La ventana activa permanece activa.</span><span class="sxs-lookup"><span data-stu-id="457c3-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="457c3-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="457c3-149">Abra la aplicación con su ventana en el estado predeterminado especificado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="457c3-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="457c3-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="457c3-150">Remarks</span></span>

<span data-ttu-id="457c3-151">Este método se implementa y se accede a través del [**método Shell.ShellExecute.**](./shell-shellexecute.md)</span><span class="sxs-lookup"><span data-stu-id="457c3-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="457c3-152">Este método equivale a iniciar uno de los comandos asociados al menú contextual de un archivo.</span><span class="sxs-lookup"><span data-stu-id="457c3-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="457c3-153">Cada comando se representa mediante una cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="457c3-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="457c3-154">El conjunto de verbos admitidos varía de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="457c3-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="457c3-155">El verbo más comúnmente admitido es "open", que también suele ser el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="457c3-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="457c3-156">Otros verbos solo pueden ser compatibles con determinados tipos de archivos.</span><span class="sxs-lookup"><span data-stu-id="457c3-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="457c3-157">Para obtener más información sobre los verbos de Shell, vea [Iniciar aplicaciones](launch.md) o [Ampliar menús contextuales.](context.md)</span><span class="sxs-lookup"><span data-stu-id="457c3-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="457c3-158">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="457c3-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="457c3-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="457c3-159">Examples</span></span>

<span data-ttu-id="457c3-160">En los ejemplos siguientes se muestra el uso de **ShellExecute para** abrir el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="457c3-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="457c3-161">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="457c3-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="457c3-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="457c3-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="457c3-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="457c3-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="457c3-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="457c3-164">Requirements</span></span>



| <span data-ttu-id="457c3-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="457c3-165">Requirement</span></span> | <span data-ttu-id="457c3-166">Valor</span><span class="sxs-lookup"><span data-stu-id="457c3-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457c3-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="457c3-167">Minimum supported client</span></span><br/> | <span data-ttu-id="457c3-168">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="457c3-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="457c3-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="457c3-169">Minimum supported server</span></span><br/> | <span data-ttu-id="457c3-170">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="457c3-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="457c3-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="457c3-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="457c3-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="457c3-173">Idl</span><span class="sxs-lookup"><span data-stu-id="457c3-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="457c3-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="457c3-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="457c3-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="457c3-176"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
