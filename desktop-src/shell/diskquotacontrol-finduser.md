---
description: Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.
title: DiskQuotaControl. FindUser, método
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
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984254"
---
# <a name="diskquotacontrolfinduser-method"></a>DiskQuotaControl. FindUser, método

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

Tipo: **String**

Valor de cadena que contiene el nombre de inicio de sesión del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.

## <a name="remarks"></a>Observaciones

Este método devuelve un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) incluso si no hay ninguna entrada para el usuario en el archivo de cuota. El objeto de usuario devuelto tiene el umbral de advertencia y los límites de cuota máxima establecidos en los valores predeterminados del volumen.

La cadena devuelta por [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) se puede pasar en lugar del parámetro *sLogonName* . Cuando **FindUser** recibe una cadena de SID, utiliza el SID correspondiente para la búsqueda directa del registro de cuota del usuario en el volumen. Esto omite la memoria caché de nombres de SID. En los casos en los que se produce un error de **FindUser** debido a una falta de coincidencia en el formato (por ejemplo, Sam-compatible y UPN) del nombre de inicio de sesión proporcionado y el nombre de inicio de sesión en caché, el nombre de inicio de sesión se puede traducir a una cadena de SID con **TranslateLogonNameToSID** , que se pasa de nuevo a **FindUser**. En el código de VBScript siguiente se muestra esta técnica.


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
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




