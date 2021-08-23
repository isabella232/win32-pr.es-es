---
title: Propiedad WebViewFolderContents.ViewOptions (Shldisp.h)
description: Obtiene un conjunto de marcas ShellFolderViewOptions que indican las opciones actuales de la vista.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- ViewOptions property Legacy Windows Environment Features
- Propiedad ViewOptions heredada Windows environment features , objeto WebViewFolderContents
- Objeto WebViewFolderContents Heredado Windows Environment Features , Propiedad ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607745"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Propiedad WebViewFolderContents.ViewOptions

Obtiene un conjunto de [**marcas ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indican las opciones actuales de la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de opciones de vista.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de esta propiedad en JScript incrustada en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

