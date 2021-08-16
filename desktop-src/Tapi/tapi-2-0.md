---
description: TAPI 2.0 proporciona un pequeño número de mejoras a la funcionalidad básica de TAPI 1.4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926def5cf2348396b9197a83e17b35d9a91d4dee617e00abe4c02d0428f2884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861251"
---
# <a name="tapi-20"></a>TAPI 2.0

TAPI 2.0 proporciona un pequeño número de mejoras a la funcionalidad básica de TAPI 1.4. Sin embargo, hubo algunos cambios arquitectónicos importantes que mejoraron enormemente su estabilidad. La mayoría de los cambios fueron cambios fundamentales necesarios para llevar TAPI a Windows NT 4.0 y aprovechar sus características (compatibilidad completa de 32 bits, servicios y Unicode). Sin embargo, estos cambios eran internos de TAPI y tenían poco efecto en las aplicaciones TAPI.

Las aplicaciones que admiten TAPI 1.3 y 1.4 (aplicaciones de 16 bits mediante una capa thunking) funcionan bien en sistemas operativos Windows Server 2003, Windows XP, Windows 2000 y Windows NT. Sin embargo, el efecto en los desarrolladores de proveedores de servicios era significativo. Los proveedores de servicios para estos sistemas operativos deben ser archivos DLL Unicode de 32 bits que se puedan ejecutar en el contexto de TAPISRV, no en el contexto de la aplicación TAPI (como todos los TSP basados en Win16 anteriores). Los TSP diseñados para TAPI 1.4 no funcionan en sistemas operativos Windows Server 2003, Windows XP, Windows 2000 o Windows NT.

TAPI 2.0 también agrega las características importantes de la compatibilidad con el centro de llamadas y la compatibilidad con calidad de servicio (QOS).

Los archivos binarios del sistema TAPI que Windows admiten las versiones 1.3 y 1.4 de TAPI para todas las aplicaciones. Sin embargo, las aplicaciones de 16 bits no pueden usar TAPI 2.0 y no se puede usar un TSP de TAPI 2.x de 16 bits.

 

 



