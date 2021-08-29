---
description: Ejecuta un verbo en un elemento de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Método ShellFolderItem.InvokeVerbEx (Shldisp.h)
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
ms.openlocfilehash: 494c6b2926b204225b4afbf41b6271209f8be0abab4432f242ef4a5bd9c26cff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884425"
---
# <a name="shellfolderiteminvokeverbex-method"></a>Método ShellFolderItem.InvokeVerbEx

Ejecuta un verbo en un elemento de Shell.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vVerb* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Variante **que** contiene la cadena verbal que corresponde al comando que se va a ejecutar. Debe ser uno de los valores devueltos por la propiedad [**Name del**](folderitemverb-name.md) elemento. Si no se especifica ningún verbo, se ejecuta el verbo predeterminado.

</dd> <dt>

*vArgs* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Variante **que** consta de una cadena con uno o varios argumentos para el comando especificado por *vVerb*. El formato de esta cadena depende del verbo concreto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Un verbo es una cadena que se usa para especificar una acción determinada que admite un elemento. Normalmente, al llamar a un verbo se inicia una aplicación relacionada. Por ejemplo, al llamar al **verbo abierto** en un archivo .txt normalmente se abre el archivo con un editor de texto, normalmente Microsoft Bloc de notas. El [**objeto FolderItemVerbs**](folderitemverbs.md) representa la colección de verbos asociados al elemento. Para obtener más información sobre los verbos, vea [Iniciar aplicaciones.](launch.md)

Este método es similar a [**InvokeVerb,**](folderitem-invokeverb.md)pero permite especificar argumentos para el comando, así como para el propio comando.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso adecuado de este método en JScript, VBScript y Visual Basic.

JScript:


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



Vbscript:


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



Visual Basic:


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




