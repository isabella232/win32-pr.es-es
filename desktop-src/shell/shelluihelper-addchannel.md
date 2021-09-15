---
description: Agrega un nuevo canal a la lista de canales del menú Windows Internet Explorer Favoritos y a la barra Canal del escritorio.
title: Método ShellUIHelper.AddChannel (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574509"
---
# <a name="shelluihelperaddchannel-method"></a>Método ShellUIHelper.AddChannel

Agrega un nuevo canal a la lista de **canales** del menú Windows Internet Explorer Favoritos y a la barra **Canal** del escritorio.

> [!Note]  
> Este método ya no se admite en Windows Vista. En ese sistema operativo, devuelve E \_ NOTIMPL.

 

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sURL* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que especifica la dirección URL del archivo CDF.

> [!Note]  
> Los vínculos del archivo CDF deben usar los protocolos HTTP, HTTPS o FTP. Si el archivo CDF contiene cualquier otro protocolo, se produce un error en la adición del canal y no aparece ningún cuadro de diálogo.

 

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML y Visual Basic.

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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
