---
description: Convierte la hora local del equipo en hora universal coordinada (hora del meridiano de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. LocalTimeToUTCTime (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689908"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Utilities. LocalTimeToUTCTime (método)

\[El método **LocalTimeToUTCTime** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El método **LocalTimeToUTCTime** convierte la hora local del equipo a la hora universal coordinada (hora del meridiano de Greenwich).

## <a name="syntax"></a>Sintaxis


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Localtime* \[ de\]
</dt> <dd>

La hora local que se va a convertir en hora universal coordinada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Hora universal coordinada que corresponde a la hora local especificada.

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

 

 




