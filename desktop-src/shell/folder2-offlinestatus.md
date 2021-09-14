---
description: Contiene el estado sin conexión de la carpeta.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Propiedad Folder2.OfflineStatus (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363123"
---
# <a name="folder2offlinestatus-property"></a>Propiedad Folder2.OfflineStatus

Contiene el estado sin conexión de la carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Valor de propiedad

Entero **que** se establece en uno de los valores siguientes.

<dt>



 (OFS) \_ DIRTYCACHE)


</dt> <dd>

El servidor está en línea con cambios no sincronizados.

</dd> <dt>



 (OFS) \_ INACTIVO)


</dt> <dd>

El almacenamiento en caché sin conexión no está habilitado para esta carpeta.

</dd> <dt>



 (OFS) \_ OFFLINE)


</dt> <dd>

El servidor está sin conexión.

</dd> <dt>



 (OFS) \_ ONLINE)


</dt> <dd>

El servidor está en línea.

</dd> <dt>



 (OFS) \_ SERVERBACK)


</dt> <dd>

El servidor está sin conexión, pero se puede acceder a él.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> Archivos sin conexión debe habilitarse a través de Opciones de carpeta para **que OfflineStatus** funcione correctamente. Si la Archivos sin conexión no está habilitada, la propiedad devuelve **OFS \_ INACTIVE**.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de **OfflineStatus** para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
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
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Carpeta2**](folder2-object.md)
</dt> <dt>

[**Carpeta**](folder.md)
</dt> </dl>

 

 




