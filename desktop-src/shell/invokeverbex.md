---
description: Ejecuta un verbo en un elemento de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Método ShellFolderItem. InvokeVerbEx (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984739"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="381d0-103">ShellFolderItem. InvokeVerbEx, método</span><span class="sxs-lookup"><span data-stu-id="381d0-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="381d0-104">Ejecuta un verbo en un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="381d0-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="381d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="381d0-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="381d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="381d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381d0-107">*vVerb* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="381d0-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="381d0-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="381d0-108">Type: **Variant**</span></span>

<span data-ttu-id="381d0-109">**Variante** que contiene la cadena de verbo que corresponde al comando que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="381d0-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="381d0-110">Debe ser uno de los valores devueltos por la propiedad [**Name**](folderitemverb-name.md) del elemento.</span><span class="sxs-lookup"><span data-stu-id="381d0-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="381d0-111">Si no se especifica ningún verbo, se ejecuta el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="381d0-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="381d0-112">*vArgs* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="381d0-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="381d0-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="381d0-113">Type: **Variant**</span></span>

<span data-ttu-id="381d0-114">**Variante** que consta de una cadena con uno o más argumentos para el comando especificado por *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="381d0-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="381d0-115">El formato de esta cadena depende del verbo determinado.</span><span class="sxs-lookup"><span data-stu-id="381d0-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="381d0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="381d0-116">Remarks</span></span>

<span data-ttu-id="381d0-117">Un verbo es una cadena que se usa para especificar una acción determinada que admite un elemento.</span><span class="sxs-lookup"><span data-stu-id="381d0-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="381d0-118">Normalmente, al llamar a un verbo se inicia una aplicación relacionada.</span><span class="sxs-lookup"><span data-stu-id="381d0-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="381d0-119">Por ejemplo, al llamar al verbo **Open** en un archivo. txt, normalmente se abre el archivo con un editor de texto, normalmente el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="381d0-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="381d0-120">El objeto [**FolderItemVerbs**](folderitemverbs.md) representa la colección de verbos asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="381d0-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="381d0-121">Para obtener más información sobre los verbos, consulte [Launching Applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="381d0-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="381d0-122">Este método es similar a [**InvokeVerb**](folderitem-invokeverb.md), pero permite especificar argumentos para el comando, así como el propio comando.</span><span class="sxs-lookup"><span data-stu-id="381d0-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="381d0-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="381d0-123">Examples</span></span>

<span data-ttu-id="381d0-124">En los siguientes ejemplos se muestra el uso correcto de este método en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="381d0-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="381d0-125">JScript.net</span><span class="sxs-lookup"><span data-stu-id="381d0-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="381d0-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="381d0-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="381d0-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="381d0-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="381d0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="381d0-128">Requirements</span></span>



| <span data-ttu-id="381d0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="381d0-129">Requirement</span></span> | <span data-ttu-id="381d0-130">Value</span><span class="sxs-lookup"><span data-stu-id="381d0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="381d0-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="381d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="381d0-132">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="381d0-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="381d0-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="381d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="381d0-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="381d0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="381d0-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="381d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="381d0-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="381d0-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="381d0-137">IDL</span><span class="sxs-lookup"><span data-stu-id="381d0-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="381d0-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="381d0-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="381d0-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="381d0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="381d0-140"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="381d0-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381d0-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="381d0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381d0-142">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="381d0-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="381d0-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="381d0-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




