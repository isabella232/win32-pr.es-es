---
description: Asigna una cuota de disco no predeterminada a un nuevo usuario.
title: Método DiskQuotaControl.AddUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579617"
---
# <a name="diskquotacontroladduser-method"></a>Método DiskQuotaControl.AddUser

Asigna una cuota de disco no predeterminada a un nuevo usuario.

## <a name="syntax"></a>Sintaxis


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **CHAR**

Valor de cadena que contiene el nombre de inicio de sesión del usuario. Use la [**propiedad UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar cómo se va a resolver el nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **Objeto**

Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.

## <a name="remarks"></a>Observaciones

El sistema de archivos NTFS crea automáticamente una entrada de cuota de usuario cuando un usuario escribe por primera vez en el volumen. A las entradas que se crean de esta manera se les asignan los valores predeterminados de umbral de advertencia y límite de cuota fija para el volumen. Este método permite crear una entrada de cuota de usuario antes de que un usuario escriba información en el volumen. Devuelve un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para asignar un umbral de advertencia o un valor de límite de cuota que difiere de la configuración predeterminada del volumen.

Si el usuario ya existe, no se crea ninguna entrada nueva. El método devuelve el [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) asociado a la entrada existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




