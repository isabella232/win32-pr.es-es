---
description: 'AM_RATE_ResetOnTimeDisc propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42b8e9d158f644d9e630555d96bf4d06e4ea9ef3cddced67742c057d0ab3859
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079525"
---
# <a name="am_rate_resetontimedisc-property"></a>Propiedad \_ \_ RESETOnTimeDisc de AM RATE

Se aplica a Windows Vista y versiones posteriores.

Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe una muestra con la marca de discontinuidad.

Esta propiedad es de lectura y escritura.



| Etiqueta | Valor |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |
| Id. de propiedad       | AM \_ RATE \_ ResetOnTimeDisc     |
| Tipo de datos         | **DWORD**                     |



 

## <a name="remarks"></a>Comentarios

Esta propiedad admite cambios de velocidad sin problemas. Si el valor de esta propiedad es **TRUE** y el descodificador recibe un ejemplo de entrada con la marca \_ AM SAMPLE TIMEDISCONTINUITY, el marco descodificado debe tener la misma marca de tiempo que el marco de \_ entrada.

Para recuperar la marca \_ AM SAMPLE \_ TIMEDISCONTINUITY, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. La marca se establece en el **miembro dwSampleFlags** de la [**estructura PROPIEDADES DE AM \_ \_ SAMPLE2.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




