---
description: Convierte la hora local del equipo en hora universal coordinada (hora media de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Método Utilities.LocalTimeToUTCTime
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
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971026"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Método Utilities.LocalTimeToUTCTime

\[El **método LocalTimeToUTCTime** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

El **método LocalTimeToUTCTime** convierte la hora local del equipo en hora universal coordinada (hora media de Greenwich).

## <a name="syntax"></a>Sintaxis


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LocalTime* \[ En\]
</dt> <dd>

Hora local que se va a convertir a hora universal coordinada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Hora universal coordinada que corresponde a la hora local especificada.

## <a name="remarks"></a>Comentarios

Aunque el sistema usa la hora universal coordinada internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y hora del día para la zona horaria local del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Utilidades**](utilities.md)
</dt> </dl>

 

 




