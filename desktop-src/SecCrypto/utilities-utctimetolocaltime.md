---
description: Convierte la hora universal coordinada (hora del meridiano de Greenwich) en la hora local del equipo.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities. UTCTimeToLocalTime (método)
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
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689907"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Utilities. UTCTimeToLocalTime (método)

\[El método **UTCTimeToLocalTime** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El método **UTCTimeToLocalTime** convierte la hora universal coordinada (hora del meridiano de Greenwich) en la hora local del equipo.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UTCTime* \[ de\]
</dt> <dd>

Hora universal coordinada que se va a convertir en la hora local del equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La hora local que corresponde a la hora universal coordinada especificada.

## <a name="remarks"></a>Observaciones

Aunque el sistema utiliza la hora universal coordinada internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y la hora del día de la zona horaria local del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sectores públicos**](utilities.md)
</dt> </dl>

 

 




