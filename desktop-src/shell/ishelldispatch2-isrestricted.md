---
description: 'Método IShellDispatch2.IsRestricted: recupera la configuración de restricción de un grupo del Registro.'
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Método IShellDispatch2.IsRestricted (Shldisp.h)
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
ms.openlocfilehash: 73bbaaefbe12e178a8ef5818665f97d29cc105e45c20c010a6c02254ab897b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710385"
---
# <a name="ishelldispatch2isrestricted-method"></a>Método IShellDispatch2.IsRestricted

Recupera la configuración de restricción de un grupo del Registro.

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

*sGroup* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre del grupo. Este valor es el nombre de una subclave del Registro con la que se va a comprobar la restricción.

</dd> <dt>

*sRestriction* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene la restricción cuyo valor se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Entero**

Valor de la restricción. Si no se encuentra la restricción especificada, el valor devuelto es 0.

### <a name="vb"></a>VB

Tipo: **\* Entero**

Valor de la restricción. Si no se encuentra la restricción especificada, el valor devuelto es 0.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.IsRestricted.**](./shell-isrestricted.md)

**IsRestricted** busca primero un nombre de subclave que coincida *con sGroup* bajo la siguiente clave.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Las restricciones se declaran como valores de las subclaves de directiva individuales. Si la restricción denominada en *sRestriction* se encuentra en la subclave denominada *en sGroup*, **IsRestricted** devuelve el valor actual de la restricción. Si la restricción no se encuentra en **HKEY \_ LOCAL \_ MACHINE**, la misma subclave se comprueba en **HKEY \_ CURRENT \_ USER**.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **IsRestricted** para recuperar el valor de datos de la restricción **undockwithoutlogon** de la subclave **System.** El uso se muestra para JScript y VBScript.

JScript:


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



Vbscript:


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
