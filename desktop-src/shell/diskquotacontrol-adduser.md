---
description: Asigna una cuota de disco no predeterminada a un nuevo usuario.
title: DiskQuotaControl. AddUser (método)
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
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540475"
---
# <a name="diskquotacontroladduser-method"></a>DiskQuotaControl. AddUser (método)

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

Tipo: **Char**

Valor de cadena que contiene el nombre de inicio de sesión del usuario. Use la propiedad [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar cómo se va a resolver el nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **Object**

Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.

## <a name="remarks"></a>Observaciones

El sistema de archivos NTFS crea automáticamente una entrada de cuota de usuario la primera vez que un usuario escribe en el volumen. A las entradas que se crean de esta manera se les asignan los valores de umbral de advertencia y límite de cuota máxima predeterminados para el volumen. Este método permite crear una entrada de cuota de usuario antes de que un usuario escriba información en el volumen. Devuelve un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para asignar un umbral de advertencia o un valor de límite de cuota que difiere de la configuración predeterminada del volumen.

Si el usuario ya existe, no se crea ninguna entrada nueva. El método devuelve el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) asociado a la entrada existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




