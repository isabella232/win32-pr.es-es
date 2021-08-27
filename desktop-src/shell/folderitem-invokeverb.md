---
description: Ejecuta un verbo en el elemento.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Método FolderItem.InvokeVerb (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111795"
---
# <a name="folderiteminvokeverb-method"></a>Método FolderItem.InvokeVerb

Ejecuta un verbo en el elemento.

## <a name="syntax"></a>Sintaxis


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vVerb* \[ in, opcional\]
</dt> <dd>

Tipo: **Variant**

Cadena que especifica el verbo que se va a ejecutar. Debe ser uno de los valores devueltos por la propiedad [**FolderItemVerb.Name**](folderitemverb-name.md) elemento. Si no se especifica ningún verbo, se invocará el verbo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un verbo es una cadena que se usa para especificar una acción determinada que admite un elemento. Invocar un verbo equivale a seleccionar un comando en el menú contextual de un elemento. Normalmente, al invocar un verbo se inicia una aplicación relacionada. Por ejemplo, al invocar el verbo "abrir" en un archivo .txt se abre el archivo con un editor de texto, normalmente Microsoft Bloc de notas. Consulte [Inicio de aplicaciones para](launch.md) obtener más información sobre los verbos.

El [**objeto FolderItemVerbs**](folderitemverbs.md) representa la colección de verbos asociados al elemento. El verbo predeterminado puede variar para distintos elementos, pero normalmente es "abierto".

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa InvokeVerb para** invocar el verbo predeterminado ("open" en este caso) en la Windows predeterminada. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verbos**](folderitem-verbs.md)
</dt> <dt>

[**Doit**](folderitemverb-doit.md)
</dt> </dl>

 

 




