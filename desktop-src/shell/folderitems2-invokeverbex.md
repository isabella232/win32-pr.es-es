---
description: Ejecuta un verbo en una colección de objetos carpeta. Este método es una extensión del método InvokeVerb, lo que permite un control adicional de la operación a través de un conjunto de marcas.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Método FolderItems2. InvokeVerbEx (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984167"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="61475-104">FolderItems2. InvokeVerbEx, método</span><span class="sxs-lookup"><span data-stu-id="61475-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="61475-105">Ejecuta un verbo en una colección de objetos [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="61475-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="61475-106">Este método es una extensión del método [**InvokeVerb**](folderitem-invokeverb.md) , lo que permite un control adicional de la operación a través de un conjunto de marcas.</span><span class="sxs-lookup"><span data-stu-id="61475-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="61475-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61475-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="61475-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61475-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61475-109">*vVerb* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="61475-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61475-110">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="61475-110">Type: **Variant**</span></span>

<span data-ttu-id="61475-111">**Variante** con la cadena de verbo que corresponde al comando que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="61475-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="61475-112">Si no se especifica ningún verbo, se ejecuta el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="61475-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="61475-113">*vArgs* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="61475-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61475-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="61475-114">Type: **Variant**</span></span>

<span data-ttu-id="61475-115">**Variante** que consta de una cadena con uno o más argumentos para el comando especificado por *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="61475-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="61475-116">El formato de esta cadena depende del verbo determinado.</span><span class="sxs-lookup"><span data-stu-id="61475-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61475-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61475-117">Remarks</span></span>

<span data-ttu-id="61475-118">Un verbo es una cadena que se usa para especificar una acción determinada asociada a un elemento o colección de elementos.</span><span class="sxs-lookup"><span data-stu-id="61475-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="61475-119">Normalmente, al llamar a un verbo se inicia una aplicación relacionada.</span><span class="sxs-lookup"><span data-stu-id="61475-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="61475-120">Por ejemplo, al llamar al verbo **Open** en un archivo. txt, normalmente se abre el archivo con un editor de texto, normalmente el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61475-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="61475-121">Para obtener más información sobre los verbos, consulte [Launching Applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="61475-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61475-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61475-122">Examples</span></span>

<span data-ttu-id="61475-123">En el ejemplo siguiente se usa **InvokeVerbEx** para invocar el verbo predeterminado ("Open") en **mi PC**.</span><span class="sxs-lookup"><span data-stu-id="61475-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="61475-124">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61475-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="61475-125">JScript.net</span><span class="sxs-lookup"><span data-stu-id="61475-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="61475-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="61475-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="61475-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="61475-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="61475-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61475-128">Requirements</span></span>



| <span data-ttu-id="61475-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="61475-129">Requirement</span></span> | <span data-ttu-id="61475-130">Value</span><span class="sxs-lookup"><span data-stu-id="61475-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61475-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61475-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61475-132">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="61475-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61475-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61475-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61475-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="61475-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="61475-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61475-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="61475-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61475-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="61475-137">IDL</span><span class="sxs-lookup"><span data-stu-id="61475-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61475-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61475-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="61475-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61475-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61475-140"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="61475-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61475-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="61475-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61475-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="61475-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="61475-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="61475-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




