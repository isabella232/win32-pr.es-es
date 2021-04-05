---
title: Propiedad WebViewFolderContents. ViewOptions (Shldisp. h)
description: Obtiene un conjunto de marcas ShellFolderViewOptions que indican las opciones actuales de la vista.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Propiedad ViewOptions características de entorno heredado de Windows
- Propiedad ViewOptions características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, propiedad ViewOptions
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
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078958"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Propiedad WebViewFolderContents. ViewOptions

Obtiene un conjunto de marcas [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indican las opciones actuales de la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de opciones de vista.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript incrustado en HTML.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

