---
description: Ejecuta un verbo en una colección de objetos FolderItem. Este método es una extensión del método InvokeVerb, lo que permite un control adicional de la operación a través de un conjunto de marcas.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Método FolderItems2.InvokeVerbEx (Shldisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363099"
---
# <a name="folderitems2invokeverbex-method"></a>Método FolderItems2.InvokeVerbEx

Ejecuta un verbo en una colección de [**objetos FolderItem.**](folderitem.md) Este método es una extensión del [**método InvokeVerb,**](folderitem-invokeverb.md) lo que permite un control adicional de la operación a través de un conjunto de marcas.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vVerb* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Variante **con** la cadena de verbo que corresponde al comando que se va a ejecutar. Si no se especifica ningún verbo, se ejecuta el verbo predeterminado.

</dd> <dt>

*vArgs* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Variante **que** consta de una cadena con uno o varios argumentos para el comando especificado por *vVerb*. El formato de esta cadena depende del verbo concreto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un verbo es una cadena que se usa para especificar una acción determinada asociada a un elemento o colección de elementos. Normalmente, al llamar a un verbo se inicia una aplicación relacionada. Por ejemplo, al llamar al **verbo** abierto en un archivo .txt normalmente se abre el archivo con un editor de texto, normalmente Microsoft Bloc de notas. Para obtener más información sobre los verbos, vea [Iniciar aplicaciones.](launch.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa InvokeVerbEx para** invocar el verbo predeterminado ("open") **en Mi PC**. Se muestra el uso adecuado para JScript, VBScript y Visual Basic.

JScript:


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



Vbscript:


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



Visual Basic:


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




