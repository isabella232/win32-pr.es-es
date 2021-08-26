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
ms.openlocfilehash: ce060c7eddb76491480f4a1de9f477629da489ae9d8412adc02da25b8d7a0a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039865"
---
# <a name="sessioncomponentcurrentstate-property"></a>Propiedad Session.ComponentCurrentState

La **propiedad ComponentCurrentState** del [**objeto Session**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte [**la propiedad ComponentRequestState.**](session-componentrequeststate.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido del componente solicitado, clave principal en la tabla Componente.

## <a name="remarks"></a>Comentarios

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session-object.md)
</dt> <dt>

[**ComponentRequestState, propiedad**](session-componentrequeststate.md)
</dt> </dl>

 

 




