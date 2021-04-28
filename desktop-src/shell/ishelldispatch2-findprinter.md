---
description: 'Método IShellDispatch2.FindPrinter: muestra el cuadro de diálogo Buscar impresora.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Método IShellDispatch2.FindPrinter (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117123"
---
# <a name="ishelldispatch2findprinter-method"></a>Método IShellDispatch2.FindPrinter

Muestra el **cuadro de diálogo Buscar** impresora.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ en, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre de la impresora.

</dd> <dt>

*sLocation* \[ en, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene la ubicación de la impresora.

</dd> <dt>

*sModel* \[ en, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el modelo de impresora.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a este método a través [**del método Shell.FindPrinter.**](./shell-findprinter.md)

Si asigna cadenas a uno o varios de los parámetros opcionales, se muestran  como valores predeterminados en el control de edición asociado cuando se muestra el cuadro de diálogo Buscar impresora. El usuario puede aceptar o invalidar estos valores. Si no se asigna ningún valor a un parámetro, el cuadro de edición asociado está vacío y el usuario debe escribir un valor.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de FindPrinter para** mostrar el cuadro de **diálogo** Buscar impresora de una aplicación determinada. El uso se muestra para JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
