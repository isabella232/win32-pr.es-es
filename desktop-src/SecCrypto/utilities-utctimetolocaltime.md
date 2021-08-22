---
description: Convierte la hora universal coordinada (hora media de Greenwich) en la hora local del equipo.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Método Utilities.UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005153"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Método Utilities.UTCTimeToLocalTime

\[El **método UTCTimeToLocalTime** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

El **método UTCTimeToLocalTime** convierte la hora universal coordinada (hora media de Greenwich) a la hora local del equipo.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HORA UTC* \[ En\]
</dt> <dd>

Hora universal coordinada que se va a convertir a la hora local del equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Hora local que corresponde a la hora universal coordinada especificada.

## <a name="remarks"></a>Comentarios

Aunque el sistema usa la hora universal coordinada internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y hora del día de la zona horaria local del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Utilidades**](utilities.md)
</dt> </dl>

 

 




