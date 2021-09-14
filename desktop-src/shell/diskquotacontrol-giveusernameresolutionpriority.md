---
description: Coloca el objeto de usuario especificado a continuación en línea para la resolución de nombres.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Método DiskQuotaControl.GiveUserNameResolutionPriority (Dskquota.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363166"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>Método DiskQuotaControl.GiveUserNameResolutionPriority

Coloca el objeto de usuario especificado a continuación en línea para la resolución de nombres.

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

Tipo: **Objeto**

Expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la resolución asincrónica de nombres está habilitada, los objetos de usuario se colocan en una cola. De forma predeterminada, se atendidas en el orden en que se colocan en la cola. El **método GiveUserNameResolutionPriority** mueve un objeto al principio de la cola para que sea el siguiente en línea al que se va a atender.

Use la [**propiedad UserNameResolution**](diskquotacontrol-usernameresolution.md) para habilitar la resolución asincrónica de nombres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




