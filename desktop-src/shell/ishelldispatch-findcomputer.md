---
description: método IShellDispatch.FindComputer: "Muestra el cuadro de diálogo Resultados de la búsqueda: Equipos. El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado."
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type: 
- APIRef
- kbSyntax api_name: 
- IShellDispatch.FindComputer api_type: 
- Com api_location: 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>Método IShellDispatch.FindComputer

Muestra el cuadro **de diálogo Resultados de la búsqueda:** Equipos . El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.FindComputer.**](shell-findcomputer.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **FindComputer** en JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



Vbscript:


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




