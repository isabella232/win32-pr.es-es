---
description: Recupera el objeto FolderItemVerb para un elemento especificado de la colección.
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
title: Método FolderItemVerbs. Item (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 013215af3f5005e68b396312d0ef13fa974d8a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985490"
---
# <a name="folderitemverbsitem-method"></a>FolderItemVerbs. Item (método)

Recupera el objeto [**FolderItemVerb**](folderitemverb.md) para un elemento especificado de la colección.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = FolderItemVerbs.Item(
  iIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iIndex* \[ de\]
</dt> <dd>

Tipo: **variante**

Índice de base cero del elemento que se va a recuperar. Este valor debe ser menor que el valor de la propiedad [**Count**](folderitemverbs-count.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Objeto que recibe el objeto [**FolderItemVerb**](folderitemverb.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **Item** para recuperar los primeros verbos de la colección disponible en la carpeta del panel de control y se muestra su nombre. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnFolderItemVerbsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);

        if (objFolder2 != null)
        {
            var objVerbs;
            objVerbs = objFolder2.Self.Verbs();
 
            if (objVerbs != null)
            {
                var objFolderItemVerb;
                objFolderItemVerb = objVerbs.Item(0);
 
                if (objFolderItemVerb != null)
                {
                    alert(objFolderItemVerb.Name);
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemVerbsItemVB()
        dim objShell
        dim objFolder2
        dim ssfCONTROLS
        
        ssfCONTROLS = 3
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfCONTROLS)
        if (not objFolder2 is nothing) then
            dim objVerbs
            set objVerbs = objFolder2.Self.Verbs

            if (not objVerbs is nothing) then
                dim objFolderItemVerb
                set objFolderItemVerb = objVerbs.Item(0)

                if (not objFolderItemVerb is nothing) then
                    alert(objFolderItemVerb.Name)
                end if

                set objFolderItemVerb = nothing
            end if

            set objVerbs = nothing
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItemVerbsItemVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfCONTROLS As Long
            
    ssfCONTROLS = 3
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)

    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        Set objVerbs = objFolder2.Self.Verbs

        If (Not objVerbs Is Nothing) Then
            Dim objFolderItemVerb As FolderItemVerb
            Set objFolderItemVerb = objVerbs.Item(0)

            If (Not objFolderItemVerb Is Nothing) Then
                Debug.Print objFolderItemVerb.Name
            End If

            Set objFolderItemVerb = Nothing
        End If

        Set objVerbs = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
