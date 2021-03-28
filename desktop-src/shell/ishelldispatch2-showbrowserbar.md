---
description: Muestra una barra del explorador.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Método IShellDispatch2. ShowBrowserBar (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984667"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>IShellDispatch2. ShowBrowserBar, método

Muestra una barra del explorador.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sCLSID* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene la forma de cadena del CLSID de la barra del explorador que se va a mostrar. El objeto se debe registrar como un objeto de barra del explorador con una \_ categoría de componente CATID InfoBand. Para obtener más información, vea [crear barras del explorador personalizadas, bandas de herramientas y bandas del escritorio](band-objects.md).

</dd> <dt>

*vShow* \[ de\]
</dt> <dd>

Tipo: **variante**

Establézcalo en **true** para mostrar la barra del explorador o en **false** para ocultarla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **variante \** _

Devuelve _ *true** si es correcto; en caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **variante \** _

Devuelve _ *true** si es correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Este método se implementa y se obtiene acceso a él a través del método [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .

Puede mostrar una de las barras del explorador estándar estableciendo el parámetro *sCLSID* en el CLSID de esa barra del explorador. Las barras del explorador estándar y sus cadenas CLSID son las siguientes:



| Barra del explorador | Cadena CLSID                           |
|--------------|----------------------------------------|
| Favoritos    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Carpetas      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Historial      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Buscar       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **ShowBrowserBar** para mostrar la barra del explorador **Favoritos** . Se muestra el uso de JScript y VBScript.

JScript.net


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
