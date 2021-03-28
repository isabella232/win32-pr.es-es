---
description: Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Método ShellLinkObject. Resolve (Shldisp. h)
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
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986059"
---
# <a name="shelllinkobjectresolve-method"></a>ShellLinkObject. Resolve (método)

Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fFlags* \[ de\]
</dt> <dd>

Tipo: **Integer**

Marcas que especifican la acción que se va a realizar. Puede ser una combinación de los siguientes valores:

<dt>



 (1)


</dt> <dd>

No muestre un cuadro de diálogo si no se puede resolver el vínculo. Cuando se establece esta marca, la palabra de orden superior de *fFlags* especifica una duración de tiempo de espera, en milisegundos. El método devuelve si no se puede resolver el vínculo dentro de la duración del tiempo de espera. Si la palabra de orden superior se establece en cero, la duración de tiempo de espera predeterminada es de 3000 milisegundos (3 segundos).

</dd> <dt>



 (4)


</dt> <dd>

Si el vínculo ha cambiado, actualice su ruta de acceso y la lista de identificadores.

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

No utilice el seguimiento de vínculos distribuidos.

</dd> <dt>



 (64)


</dt> <dd>

Deshabilite el seguimiento de vínculos distribuidos. De forma predeterminada, el seguimiento de vínculos distribuidos realiza un seguimiento de los medios extraíbles en varios dispositivos según el nombre del volumen. También utiliza la ruta de acceso UNC para realizar el seguimiento de los sistemas de archivos remotos cuya letra de unidad ha cambiado. Al establecer esta marca, se deshabilitan ambos tipos de seguimiento.

</dd> <dt>



 (128)


</dt> <dd>

Llame al Windows Installer.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Este método es esencialmente idéntico en la funcionalidad que se va a [**resolver**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Para obtener más información sobre la resolución de vínculos, vea la sección Comentarios de esa página.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript, VBScript y Visual Basic.

JScript.net


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



VBScript


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
