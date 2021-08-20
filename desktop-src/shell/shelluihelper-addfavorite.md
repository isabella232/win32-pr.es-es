---
description: Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa con los parámetros especificados.
title: Método ShellUIHelper.AddFavorite (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: f106b9860dcfa87cad9a69763731b47aeb4f9b0c7d4698f72dfc7210498e9234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676626"
---
# <a name="shelluihelperaddfavorite-method"></a>Método ShellUIHelper.AddFavorite

Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa con los parámetros especificados.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sURL* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que especifica la dirección URL del elemento que se va a agregar a la **carpeta Favoritos.**

</dd> <dt>

*vTitle* \[ en, opcional\]
</dt> <dd>

Tipo: **\* Variant**

Valor **Variant** que especifica el nombre del elemento.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertados en HTML y Visual Basic.

JScript:


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
