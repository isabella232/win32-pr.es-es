---
description: Agrega un elemento a microsoft Active Desktop.
title: Método ShellUIHelper.AddDesktopComponent (Exdisp.h)
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
ms.openlocfilehash: 5141b35b9fb71b09b9b269016d0b38cdb0b9f01ec88a02070a0f936934159930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941505"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Método ShellUIHelper.AddDesktopComponent

Agrega un elemento a microsoft Active Desktop.

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

*sURL* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que especifica la dirección URL del nuevo elemento favorito.

</dd> <dt>

*sType* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que especifica el tipo de elemento que se va a agregar. Puede ser uno de los siguientes valores.

<dt>



 (imagen)


</dt> <dd>

El componente es una imagen.

</dd> <dt>



 (sitio web)


</dt> <dd>

El componente es un sitio web.

</dd> </dl> </dd> <dt>

*Izquierda* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición del borde izquierdo del componente, en coordenadas de pantalla.

</dd> <dt>

*Parte superior* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición del borde superior del componente, en coordenadas de pantalla.

</dd> <dt>

*Ancho* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Ancho del componente, en unidades de pantalla.

</dd> <dt>

*Alto* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Alto del componente, en unidades de pantalla.

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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
