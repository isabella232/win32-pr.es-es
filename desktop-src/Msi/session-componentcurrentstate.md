---
description: La propiedad ComponentCurrentState del objeto de sesión es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte la propiedad ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Propiedad Session. ComponentCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653704"
---
# <a name="sessioncomponentcurrentstate-property"></a>Propiedad Session. ComponentCurrentState

La propiedad **ComponentCurrentState** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte la propiedad [**ComponentRequestState**](session-componentrequeststate.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido del componente solicitado, clave principal en la tabla de componentes.

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session-object.md)
</dt> <dt>

[**Propiedad ComponentRequestState**](session-componentrequeststate.md)
</dt> </dl>

 

 




