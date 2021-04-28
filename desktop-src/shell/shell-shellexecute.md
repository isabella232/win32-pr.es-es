---
description: 'Método Shell.ShellExecute: realiza una operación especificada en un archivo especificado.'
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Método Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0fd31f0859fff5a1c94d5586f287e4a8980ddc02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104133"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="37118-103">Método Shell.ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37118-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="37118-104">Realiza una operación especificada en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="37118-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="37118-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37118-105">Syntax</span></span>

<span data-ttu-id="37118-106">Jscript:</span><span class="sxs-lookup"><span data-stu-id="37118-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="37118-107">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="37118-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="37118-108">VB:</span><span class="sxs-lookup"><span data-stu-id="37118-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="37118-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37118-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37118-110">*sFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37118-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37118-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="37118-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="37118-112">Cadena **que** contiene el nombre del archivo en el que **ShellExecute** realizará la acción especificada por *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="37118-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="37118-113">*vArguments* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="37118-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37118-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37118-114">Type: **Variant**</span></span>

<span data-ttu-id="37118-115">Cadena que contiene valores de parámetro para la operación.</span><span class="sxs-lookup"><span data-stu-id="37118-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37118-116">*vDirectory* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="37118-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37118-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37118-117">Type: **Variant**</span></span>

<span data-ttu-id="37118-118">Ruta de acceso completa del directorio que contiene el archivo especificado por *sFile*.</span><span class="sxs-lookup"><span data-stu-id="37118-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="37118-119">Si no se especifica este parámetro, se usa el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="37118-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="37118-120">*vOperation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="37118-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37118-121">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37118-121">Type: **Variant**</span></span>

<span data-ttu-id="37118-122">La operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="37118-122">The operation to be performed.</span></span> <span data-ttu-id="37118-123">Este valor se establece en una de las cadenas de verbo admitidas por el archivo.</span><span class="sxs-lookup"><span data-stu-id="37118-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="37118-124">Para obtener una explicación de los verbos, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="37118-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="37118-125">Si no se especifica este parámetro, se realiza la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="37118-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="37118-126">*vShow* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="37118-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37118-127">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37118-127">Type: **Variant**</span></span>

<span data-ttu-id="37118-128">Una recomendación sobre cómo se debe mostrar inicialmente la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37118-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="37118-129">La aplicación puede omitir esta recomendación.</span><span class="sxs-lookup"><span data-stu-id="37118-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="37118-130">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="37118-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="37118-131">Si no se especifica este parámetro, la aplicación usa su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="37118-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="37118-132">Valor</span><span class="sxs-lookup"><span data-stu-id="37118-132">Value</span></span>                                                                                                                               | <span data-ttu-id="37118-133">Significado</span><span class="sxs-lookup"><span data-stu-id="37118-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37118-134"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37118-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="37118-135">Abra la aplicación con una ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="37118-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="37118-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="37118-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="37118-137">Abra la aplicación con una ventana normal.</span><span class="sxs-lookup"><span data-stu-id="37118-137">Open the application with a normal window.</span></span> <span data-ttu-id="37118-138">Si la ventana está minimizada o maximizada, el sistema la restaura a su tamaño y posición originales.</span><span class="sxs-lookup"><span data-stu-id="37118-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="37118-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="37118-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="37118-140">Abra la aplicación con una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="37118-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="37118-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="37118-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="37118-142">Abra la aplicación con una ventana maximizada.</span><span class="sxs-lookup"><span data-stu-id="37118-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="37118-143"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="37118-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="37118-144">Abra la aplicación con su ventana en su tamaño y posición más recientes.</span><span class="sxs-lookup"><span data-stu-id="37118-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="37118-145">La ventana activa permanece activa.</span><span class="sxs-lookup"><span data-stu-id="37118-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="37118-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="37118-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="37118-147">Abra la aplicación con su ventana en su tamaño y posición actuales.</span><span class="sxs-lookup"><span data-stu-id="37118-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="37118-148"><dt></dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="37118-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="37118-149">Abra la aplicación con una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="37118-149">Open the application with a minimized window.</span></span> <span data-ttu-id="37118-150">La ventana activa permanece activa.</span><span class="sxs-lookup"><span data-stu-id="37118-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="37118-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="37118-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="37118-152">Abra la aplicación con su ventana en el estado predeterminado especificado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37118-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37118-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37118-153">Remarks</span></span>

<span data-ttu-id="37118-154">Este método equivale a iniciar uno de los comandos asociados al menú contextual de un archivo.</span><span class="sxs-lookup"><span data-stu-id="37118-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="37118-155">Cada comando se representa mediante una cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="37118-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="37118-156">El conjunto de verbos admitidos varía de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="37118-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="37118-157">El verbo más admitido es "open", que también suele ser el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="37118-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="37118-158">Es posible que solo determinados tipos de archivos solo admiten otros verbos.</span><span class="sxs-lookup"><span data-stu-id="37118-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="37118-159">Para obtener más información sobre los verbos de Shell, vea [Iniciar aplicaciones](launch.md) o [Extender menús contextuales.](context.md)</span><span class="sxs-lookup"><span data-stu-id="37118-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="37118-160">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="37118-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="37118-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="37118-161">Examples</span></span>

<span data-ttu-id="37118-162">En los ejemplos siguientes se muestra el uso **de ShellExecute para** abrir el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="37118-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="37118-163">El uso se muestra para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="37118-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="37118-164">Jscript:</span><span class="sxs-lookup"><span data-stu-id="37118-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="37118-165">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="37118-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="37118-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37118-166">Requirements</span></span>



| <span data-ttu-id="37118-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="37118-167">Requirement</span></span> | <span data-ttu-id="37118-168">Valor</span><span class="sxs-lookup"><span data-stu-id="37118-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37118-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37118-169">Minimum supported client</span></span><br/> | <span data-ttu-id="37118-170">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="37118-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37118-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37118-171">Minimum supported server</span></span><br/> | <span data-ttu-id="37118-172">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37118-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="37118-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37118-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="37118-174"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="37118-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="37118-175">Idl</span><span class="sxs-lookup"><span data-stu-id="37118-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37118-176"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="37118-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="37118-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37118-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37118-178"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="37118-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
