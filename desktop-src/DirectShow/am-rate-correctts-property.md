---
description: El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está configurando las marcas de tiempo correctas en los ejemplos que entrega al descodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propiedad AM_RATE_CorrectTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690632"
---
# <a name="am_rate_correctts-property"></a>Propiedad de la frecuencia de la \_ tasa AM \_

El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está configurando las marcas de tiempo correctas en los ejemplos que entrega al descodificador.



|                   |                               |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM |
| Id. de propiedad       | Frecuencia de las \_ \_ correcciones de AM           |
| Tipo de datos         | **LONG**                      |



 

## <a name="remarks"></a>Observaciones

Las versiones anteriores del navegador de DVD no establecieron las marcas de tiempo correctas cuando la velocidad de reproducción era distinta de 1,0. Muchos descodificadores solucionan este problema pasando por alto las marcas de tiempo durante el rebobinado o avance rápido, y calculando los tiempos de presentación correctos.

Estos problemas se han corregido en la versión actual del navegador de DVD. Para la compatibilidad con versiones anteriores con los descodificadores existentes, el navegador de DVD indica que las marcas de tiempo son correctas al establecer la \_ propiedad AM Rates \_ correct en el descodificador con el valor **true**. Cuando se establece esta propiedad, el descodificador debe utilizar las marcas de tiempo reales, en lugar de estimar los tiempos de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




