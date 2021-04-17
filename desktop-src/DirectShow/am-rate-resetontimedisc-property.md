---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Propiedad AM_RATE_ResetOnTimeDisc (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690630"
---
# <a name="am_rate_resetontimedisc-property"></a>\_Propiedad ResetOnTimeDisc de tasa AM \_

Se aplica a Windows Vista y versiones posteriores.

Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe un ejemplo con la marca de discontinuidad.

Esta propiedad es de lectura y escritura.



|                   |                               |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM |
| Id. de propiedad       | Tasa de AM \_ \_ ResetOnTimeDisc     |
| Tipo de datos         | **DWORD**                     |



 

## <a name="remarks"></a>Observaciones

Esta propiedad admite cambios de velocidad sin problemas. Si el valor de esta propiedad es **true** y el descodificador recibe un ejemplo de entrada con la \_ marca TIMEDISCONTINUITY de ejemplo AM \_ , el marco descodificado debe tener la misma marca de tiempo que el marco de entrada.

Para recuperar la \_ marca TIMEDISCONTINUITY de ejemplo AM \_ , llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. La marca se establece en el miembro **dwSampleFlags** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

Para obtener más información, consulte [mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




