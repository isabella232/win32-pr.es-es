---
description: Sincroniza todos los archivos sin conexión de la carpeta .
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Método Folder2.Synchronize (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5a0865ab34c9ffba625a51881e01f5cb2df774da9e8d4a32a7fbd17f6dbf523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458895"
---
# <a name="folder2synchronize-method"></a>Método Folder2.Synchronize

Sincroniza todos los archivos sin conexión de la carpeta .

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

Para usar este método, la Archivos sin conexión debe estar habilitada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de **Synchronize** para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Carpeta2**](folder2-object.md)
</dt> <dt>

[**Carpeta**](folder.md)
</dt> </dl>

 

 




