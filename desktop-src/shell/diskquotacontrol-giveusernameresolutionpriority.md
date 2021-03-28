---
description: Coloca el objeto de usuario especificado junto a la línea para la resolución de nombres.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Método DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540467"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>DiskQuotaControl. GiveUserNameResolutionPriority, método

Coloca el objeto de usuario especificado junto a la línea para la resolución de nombres.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oUser* 
</dt> <dd>

Tipo: **Object**

Expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la resolución de nombres asincrónica está habilitada, los objetos de usuario se colocan en una cola. De forma predeterminada, se les presta servicio en el orden en que se colocan en la cola. El método **GiveUserNameResolutionPriority** mueve un objeto al principio de la cola para que sea el siguiente en la línea que se va a atender.

Use la propiedad [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para habilitar la resolución de nombres asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




