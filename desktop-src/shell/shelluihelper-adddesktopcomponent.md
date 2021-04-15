---
description: Agrega un elemento a Microsoft Active Desktop.
title: Método ShellUIHelper. AddDesktopComponent (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985955"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>ShellUIHelper. AddDesktopComponent, método

Agrega un elemento a Microsoft Active Desktop.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sURL* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor de **cadena** que especifica la dirección URL del nuevo elemento favorito.

</dd> <dt>

*SSE esperaba una* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor de **cadena** que especifica el tipo de elemento que se va a agregar. Puede ser uno de los valores siguientes.

<dt>



 impresión


</dt> <dd>

El componente es una imagen.

</dd> <dt>



 bsitio


</dt> <dd>

El componente es un sitio Web.

</dd> </dl> </dd> <dt>

*Izquierda* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Posición del borde izquierdo del componente, en coordenadas de la pantalla.

</dd> <dt>

*Parte superior* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Posición del borde superior del componente, en coordenadas de la pantalla.

</dd> <dt>

*Ancho* \[ de en, opcional\]
</dt> <dd>

Tipo: **variante**

Ancho del componente, en unidades de pantalla.

</dd> <dt>

*Alto* \[ de en, opcional\]
</dt> <dd>

Tipo: **variante**

Alto del componente, en unidades de pantalla.

</dd> </dl>

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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
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



 

 
