---
description: Recupera el valor de restricción de un grupo del registro.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Método IShellDispatch2. IsRestricted (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984694"
---
# <a name="ishelldispatch2isrestricted-method"></a>IShellDispatch2. IsRestricted, método

Recupera el valor de restricción de un grupo del registro.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sGroup* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene el nombre del grupo. Este valor es el nombre de una subclave del registro en la que se va a comprobar la restricción.

</dd> <dt>

*sRestriction* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene la restricción cuyo valor se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Type: **Integer \** _

Valor de la restricción. Si no se encuentra la restricción especificada, el valor devuelto es 0.

### <a name="vb"></a>VB

Tipo: _*Integer \**_

Valor de la restricción. Si no se encuentra la restricción especificada, el valor devuelto es 0.

## <a name="remarks"></a>Observaciones

Este método se implementa y se obtiene acceso a él mediante el método [_ *Shell. IsRestricted* *](./shell-isrestricted.md) .

**IsRestricted** busca primero un nombre de subclave que coincida con *sGroup* en la siguiente clave.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Las restricciones se declaran como valores de las subclaves de la Directiva individual. Si la restricción denominada en *sRestriction* se encuentra en la subclave denominada en *sGroup*, **IsRestricted** devuelve el valor actual de la restricción. Si no se encuentra la restricción en **HKEY \_ local \_ Machine**, se comprueba la misma subclave en **HKEY \_ Current \_ User**.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **IsRestricted** para recuperar el valor de datos de la restricción **undockwithoutlogon** de la subclave **System** . Se muestra el uso de JScript y VBScript.

JScript.net


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

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



 

 
