---
description: método Shell.FindComputer: "Muestra el cuadro de diálogo Resultados de la búsqueda: Equipos. El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado."
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type: 
- APIRef
- kbSyntax api_name: 
- Shell.FindComputer api_type: 
- Com api_location: 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Método Shell.FindComputer

Muestra el cuadro **de diálogo Resultados de la búsqueda:** Equipos . El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.

## <a name="syntax"></a>Sintaxis


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra FindComputer** en uso. El resultado de este código es  el mismo que al presionar el botón Inicio, hacer clic en **Buscar,** hacer clic en la opción Impresoras, equipos o personas y, a **continuación,** hacer clic en Un equipo de **la red.** Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




