---
description: Indica si se ha suscrito a una dirección URL especificada.
title: Método ShellUIHelper. IsSubscribed (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082809"
---
# <a name="shelluihelperissubscribed-method"></a>ShellUIHelper. IsSubscribed, método

Indica si se ha suscrito a una dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sURL* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor de **cadena** que especifica la dirección URL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **booleano \** _

_ *true** si la dirección URL está suscrita a; en caso contrario, **false**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML y Visual Basic.

JScript.net


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
