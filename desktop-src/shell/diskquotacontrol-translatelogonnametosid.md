---
description: Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.
title: Método DiskQuotaControl.TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 6bcaa5ac4f7dff4be80763b0aa411b7f104ff786b21e422044bdc7198697d54c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111825"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Método DiskQuotaControl.TranslateLogonNameToSID

Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*logonname* 
</dt> <dd>

Tipo: **Cadena**

Valor de cadena que especifica el nombre de inicio de sesión del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de seguridad de usuario (SID) en formato de cadena correspondiente al nombre de inicio de sesión proporcionado. La cadena devuelta incluye las llaves de cierre estándar. Por ejemplo:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Comentarios

La cadena SID devuelta se puede pasar al [**método FindUser**](diskquotacontrol-finduser.md) en lugar de un nombre de inicio de sesión.

Cuando se produce un error en una llamada al método [**FindUser**](diskquotacontrol-finduser.md)( *logonname*), podría deberse a una discrepancia entre el formulario (por ejemplo, compatible con SAM del Administrador de cuentas de seguridad y el UPN de nombre principal de usuario) del nombre de inicio de sesión proporcionado y el formulario almacenado en la caché \[ de nombres de \] \[ \] SID. En tales casos, el nombre de inicio de sesión se puede convertir en un SID y la llamada a **FindUser se repite.** **FindUser** reconoce una cadena de SID y omitirá la búsqueda de caché con nombre de SID. El siguiente código de Microsoft Visual Basic Scripting Edition (VBScript) ilustra esta técnica.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



La traducción de nombre a SID puede ser un proceso lento en comparación con las búsquedas en la caché de nombres de SID. Por lo tanto, se recomienda llamar primero a [**FindUser**](diskquotacontrol-finduser.md) con un nombre de inicio de sesión. En el ejemplo anterior se usa esta técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




