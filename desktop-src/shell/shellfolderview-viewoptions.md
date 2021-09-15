---
description: Obtiene un conjunto de marcas que indican las opciones actuales de la vista.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Propiedad ShellFolderView.ViewOptions (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579521"
---
# <a name="shellfolderviewviewoptions-property"></a>Propiedad ShellFolderView.ViewOptions

Obtiene un conjunto de marcas que indican las opciones actuales de la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de opciones de vista. Contiene uno o varios de los valores siguientes:

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

La **opción Mostrar todos los** archivos está habilitada.

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ SHOWEXTENSIONS** (0x00000002)


</dt> <dd>

La **opción Ocultar extensiones para tipos de archivo conocidos** está deshabilitada.

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

La **opción Mostrar archivos y carpetas comprimidos con color** alternativo está habilitada.

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

La **opción No mostrar archivos ocultos** está habilitada.

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)


</dt> <dd>

La **opción Estilo clásico** está habilitada.

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

La **opción Hacer doble clic para abrir un elemento** está habilitada.

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

La **opción Active Desktop : Ver como página web** está habilitada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local. No funcionará cuando se ejecute en una página web a través de HTTP o UNC.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método en JScript incrustado en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
