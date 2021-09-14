---
description: La propiedad ComponentCurrentState del objeto Session es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte la propiedad ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Propiedad Session.ComponentCurrentState
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063031"
---
# <a name="sessioncomponentcurrentstate-property"></a>Propiedad Session.ComponentCurrentState

La **propiedad ComponentCurrentState** del objeto [**Session**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte [**la propiedad ComponentRequestState.**](session-componentrequeststate.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido del componente solicitado, clave principal en la tabla Componente.

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Sesión**](session-object.md)
</dt> <dt>

[**ComponentRequestState, propiedad**](session-componentrequeststate.md)
</dt> </dl>

 

 




