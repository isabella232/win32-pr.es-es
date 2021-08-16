---
description: Busca el destino de un vínculo de Shell, incluso si se ha movido o cambiado el nombre del destino.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Método ShellLinkObject.Resolve (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdff3fd1a606b8dbec35476988497dd14892692a42e6502343716264873c184d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857498"
---
# <a name="shelllinkobjectresolve-method"></a>Método ShellLinkObject.Resolve

Busca el destino de un vínculo de Shell, incluso si se ha movido o cambiado el nombre del destino.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fFlags* \[ En\]
</dt> <dd>

Tipo: **Entero**

Marcas que especifican la acción que se va a realizar. Puede ser una combinación de los siguientes valores:

<dt>



 (1)


</dt> <dd>

No muestre un cuadro de diálogo si no se puede resolver el vínculo. Cuando se establece esta marca, la palabra de orden superior *de fFlags* especifica una duración de tiempo de espera, en milisegundos. El método devuelve si el vínculo no se puede resolver dentro de la duración del tiempo de espera. Si la palabra de orden superior se establece en cero, la duración del tiempo de espera se establece de forma predeterminada en 3000 milisegundos (3 segundos).

</dd> <dt>



 (4)


</dt> <dd>

Si el vínculo ha cambiado, actualice su ruta de acceso y lista de identificadores.

</dd> <dt>



 (8)


</dt> <dd>

No actualice la información del vínculo.

</dd> <dt>



 (16)


</dt> <dd>

No ejecute la heurística de búsqueda.

</dd> <dt>



 (32)


</dt> <dd>

No use el seguimiento de vínculos distribuidos.

</dd> <dt>



 (64)


</dt> <dd>

Deshabilite el seguimiento de vínculos distribuidos. De forma predeterminada, el seguimiento de vínculos distribuidos realiza un seguimiento de los medios extraíbles en varios dispositivos según el nombre del volumen. También usa la ruta de acceso UNC para realizar un seguimiento de los sistemas de archivos remotos cuya letra de unidad ha cambiado. Al establecer esta marca se deshabilitan ambos tipos de seguimiento.

</dd> <dt>



 (128)


</dt> <dd>

Llame al instalador Windows.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Este método es esencialmente idéntico en funcionalidad a [**Resolver**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Para obtener más información sobre la resolución de vínculos, consulte la sección Comentarios de esa página.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
