---
description: Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.
title: Método DiskQuotaControl.FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841526"
---
# <a name="diskquotacontrolfinduser-method"></a>Método DiskQuotaControl.FindUser

Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **Cadena**

Valor de cadena que contiene el nombre de inicio de sesión del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.

## <a name="remarks"></a>Observaciones

Este método devuelve un [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) incluso si no hay ninguna entrada para el usuario en el archivo de cuota. El objeto de usuario devuelto tiene límites de umbral de advertencia y cuota fija establecidos en los valores predeterminados del volumen.

La cadena devuelta por [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) se puede pasar en lugar del *parámetro sLogonName.* Cuando **FindUser** recibe una cadena SID, usa el SID correspondiente para la búsqueda directa del registro de cuota del usuario en el volumen. Esto omite la caché de nombres de SID. En los casos en los que **FindUser** produce un error debido a una discrepancia de formato (por ejemplo, compatible con SAM y UPN) del nombre de inicio de sesión proporcionado y el nombre de inicio de sesión almacenado en caché, el nombre de inicio de sesión se puede traducir a una cadena SID mediante **TranslateLogonNameToSID** y, a continuación, pasar de nuevo a **FindUser**. El siguiente código VBScript ilustra esta técnica.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




