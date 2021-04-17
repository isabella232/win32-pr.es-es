---
title: Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel
description: Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705052"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8 y Windows Server 2012, incluido WinPE, el kernel se ha bloqueado para evitar que el malware introducido por los kits de arranque o raíz eluda los requisitos de seguridad del sistema operativo Windows para los controladores firmados.

Este cambio afecta a todos los controladores en modo kernel para dispositivos que admiten el arranque seguro de Unified extensible firmware Interface (UEFI). El arranque seguro UEFI es necesario para la certificación de Windows 8 para equipos cliente y es opcional para los servidores. No afecta a los controladores de modo de usuario.

El desarrollo estándar para los controladores en modo kernel implica el uso de la configuración de la depuración en modo kernel o de datos de configuración de arranque (BCD) <testsigning> . Ambos están deshabilitados cuando el arranque protegido está activado.

## <a name="manifestation"></a>Manifestación

Los controladores en modo kernel no se ejecutarán si no están firmados correctamente por una entidad de certificación (CA) de confianza. El sistema operativo no permitirá la ejecución de controladores que no sean de confianza y no se permitirán mecanismos estándar como la depuración de kernel y testsigning.

## <a name="mitigation"></a>Mitigación

Para probar los controladores, debe deshabilitar el arranque seguro en BIOS y cumplir los otros requisitos de firma de prueba (consulte a continuación).

Al distribuir controladores más ampliamente, deben estar firmados correctamente por una CA de confianza.

## <a name="resources"></a>Recursos

-   [Controladores de firma](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 