---
description: 'Método Shell.TrayProperties: muestra la barra de tareas y el cuadro de diálogo Propiedades del menú Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Propiedades.'
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Método Shell.TrayProperties (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ef9ed639383b468b68f75e43f1b38b2952795ceb1990f580a766174334dadd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452831"
---
# <a name="shelltrayproperties-method"></a>Método Shell.TrayProperties

Muestra el cuadro **de diálogo Propiedades de la barra de tareas y del menú** Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Propiedades**.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra TrayProperties** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

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



 

 




