---
description: El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está estableciendo las marcas de tiempo correctas en los ejemplos que entrega al descodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162361"
---
# <a name="am_rate_correctts-property"></a>Propiedad AM \_ RATE \_ CorrectTS

El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está estableciendo las marcas de tiempo correctas en los ejemplos que entrega al descodificador.



| Etiqueta | Value |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |
| Id. de propiedad       | AM \_ RATE \_ CorrectTS           |
| Tipo de datos         | **LONG**                      |



 

## <a name="remarks"></a>Observaciones

Las versiones anteriores de DVD Navigator no establecen las marcas de tiempo correctas cuando la velocidad de reproducción era distinta de la 1.0. Muchos descodificadores funcionan para solucionar este problema omitiendo las marcas de tiempo durante el rebobinado o el avance rápido, y calculando los tiempos de presentación correctos.

Estos problemas se han corregido en la versión actual del navegador de DVD. Para la compatibilidad con versiones anteriores con los descodificadores existentes, el navegador de DVD indica que las marcas de tiempo son correctas estableciendo la propiedad AM RATE CorrectTS en el descodificador con el \_ \_ valor **TRUE**. Cuando se establece esta propiedad, el descodificador debe usar las marcas de tiempo reales, en lugar de calcular los tiempos de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)
</dt> </dl>

 

 




