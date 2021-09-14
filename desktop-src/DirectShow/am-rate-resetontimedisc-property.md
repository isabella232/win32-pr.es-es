---
description: 'AM_RATE_ResetOnTimeDisc propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162342"
---
# <a name="am_rate_resetontimedisc-property"></a>Propiedad \_ \_ RESETOnTimeDisc de AM RATE

Se aplica a Windows Vista y versiones posteriores.

Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe una muestra con la marca de discontinuidad.

Esta propiedad es de lectura y escritura.



| Etiqueta | Value |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |
| Id. de propiedad       | AM \_ RATE \_ ResetOnTimeDisc     |
| Tipo de datos         | **DWORD**                     |



 

## <a name="remarks"></a>Observaciones

Esta propiedad admite cambios de velocidad sin problemas. Si el valor de esta propiedad es **TRUE** y el descodificador recibe un ejemplo de entrada con la marca \_ AM SAMPLE TIMEDISCONTINUITY, el marco descodificado debe tener la misma marca de tiempo que el marco de \_ entrada.

Para recuperar la marca \_ AM SAMPLE \_ TIMEDISCONTINUITY, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. La marca se establece en el **miembro dwSampleFlags** de la [**estructura PROPIEDADES DE AM \_ \_ SAMPLE2.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




