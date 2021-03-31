---
description: TAPI 2,0 proporciona un pequeño número de mejoras en la funcionalidad básica de TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360684"
---
# <a name="tapi-20"></a>TAPI 2,0

TAPI 2,0 proporciona un pequeño número de mejoras en la funcionalidad básica de TAPI 1,4. Sin embargo, se han producido algunos cambios importantes en la arquitectura que mejoran considerablemente su estabilidad. La mayoría de los cambios eran cambios fundamentales necesarios para incorporar TAPI a Windows NT 4,0 y aprovechar sus características (soporte completo de 32 bits, servicios y Unicode). Sin embargo, estos cambios eran internos en TAPI y apenas tenían efecto en las aplicaciones TAPI.

Las aplicaciones que admiten TAPI 1,3 y 1,4 (aplicaciones de 16 bits por medio de una capa de sistema operativo) funcionan bien en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 y Windows NT. Sin embargo, el efecto en los desarrolladores de proveedores de servicios era significativo. Los proveedores de servicios de estos sistemas operativos deben ser archivos dll Unicode de 32 bits completamente que se puedan ejecutar en el contexto de TAPISRV, no en el contexto de la aplicación TAPI (como ocurría en todas las profesionales basadas en Win16 anteriores). Profesionales diseñado para TAPI 1,4 no funcionan en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 ni Windows NT.

TAPI 2,0 también agrega las características importantes del soporte técnico del centro de llamadas y la compatibilidad con calidad de servicio (QOS).

Los archivos binarios del sistema TAPI que incluye Windows admiten las versiones 1,3 y 1,4 de TAPI para todas las aplicaciones. Sin embargo, las aplicaciones de 16 bits no pueden usar TAPI 2,0 y no se puede usar un TSP TAPI 2. x de 16 bits.

 

 



