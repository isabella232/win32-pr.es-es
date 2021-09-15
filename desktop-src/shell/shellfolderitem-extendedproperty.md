---
description: Obtiene el valor de una propiedad del conjunto de propiedades de un elemento. La propiedad se puede especificar por nombre o por el identificador de formato (FMTID) y el identificador de propiedad (PID) del conjunto de propiedades.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Método ShellFolderItem.ExtendedProperty (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468079"
---
# <a name="shellfolderitemextendedproperty-method"></a>Método ShellFolderItem.ExtendedProperty

Obtiene el valor de una propiedad del conjunto de propiedades de un elemento. La propiedad se puede especificar por nombre o por el identificador de formato (FMTID) y el identificador de propiedad (PID) del conjunto de propiedades.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sPropName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que especifica la propiedad . Para obtener información detallada, consulte la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **\* Variant**

Cuando este método vuelve, contiene el valor de la propiedad , si existe para el elemento especificado. El valor tendrá escritura completa; por ejemplo, las fechas se devuelven como fechas, no como cadenas.

Este método devuelve una cadena de longitud cero si la propiedad es válida pero no existe para el elemento especificado, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Hay dos maneras de especificar una propiedad. La primera es asignar el nombre conocido de la propiedad, como "Author" o "Date", a *sPropName*. Sin embargo, cada propiedad es miembro de un conjunto de propiedades del Modelo de objetos componentes (COM) y también se puede identificar especificando su identificador de formato (FMTID) y el identificador de propiedad (PID). Un [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) es un GUID que identifica el conjunto de propiedades y un [**PID**](../stg/structured-storage-serialized-property-set-format.md) es un entero que identifica una propiedad determinada dentro del conjunto de propiedades.

Especificar una propiedad por sus valores FMTID/PID suele ser más eficaz que usar su nombre. Para usar los valores FMTID/PID de una propiedad **con ExtendedProperty,** deben combinarse en un SCID. Un SCID es una cadena que contiene los valores FMTID/PID con el formato *"FMTID**PID",* donde FMTID es la forma de cadena del GUID del conjunto de propiedades. Por ejemplo, el SCID de la propiedad author del conjunto de información de resumen es "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Para obtener una lista de FMTID y PID que admite actualmente el shell, vea [**SHCOLUMNID**](./objects.md).

## <a name="examples"></a>Ejemplos

Este código de ejemplo muestra cómo usar **ExtendedProperty para** recuperar las propiedades "Title" y "Author" de un documento de Word. Una vez que tenga el [**objeto ShellFolderItem**](shellfolderitem-object.md) asociado al archivo, *fiWordDoc* en este ejemplo, recupere el valor de la propiedad pasando su nombre a **ExtendedProperty**.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Un enfoque más rápido y eficaz es pasar un SCID a **ExtendedProperty.**


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



En los ejemplos siguientes se muestra el uso adecuado de este método para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
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
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
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
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
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
Private Sub fnFolderItem2ExtendedPropertyVB()
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
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
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
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
