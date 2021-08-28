---
title: Requisitos de firma de características de arranque seguras para controladores en modo kernel
description: Requisitos de firma de características de arranque seguras para controladores en modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6593df6707dc26b36fceca796c436ed45f3f0c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885068"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisitos de firma de características de arranque seguras para controladores en modo kernel

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8 y Windows Server 2012, incluido WinPE, el kernel se ha bloqueado para evitar que el malware introducido por los kits de arranque o raíz sortee los requisitos de seguridad del sistema operativo Windows los controladores firmados.

Este cambio afecta a todos los controladores en modo kernel para los dispositivos que admiten el arranque seguro unificado de la interfaz extensible de firmware (UEFI); UeFI Secure Boot es necesario para la Windows 8 para las máquinas cliente y opcional para los servidores. No afecta a los controladores en modo de usuario.

El desarrollo estándar para controladores en modo kernel implica el uso de depuración en modo kernel o la configuración de firma de pruebas de datos de configuración &lt; de arranque (BCD). &gt; Ambos se deshabilitan cuando el arranque seguro está habilitado.

## <a name="manifestation"></a>Manifestación

Los controladores en modo kernel no se ejecutarán si no están firmados correctamente por una entidad de certificación (CA) de confianza. El sistema operativo no permitirá que se ejecuten controladores que no sean de confianza y no se permitirán mecanismos estándar como la depuración del kernel y la firma de pruebas.

## <a name="mitigation"></a>Mitigación

Para probar los controladores, debe deshabilitar el arranque seguro en el BIOS, así como cumplir los demás requisitos de firma de pruebas (consulte a continuación).

Al distribuir los controladores de forma más amplia, deben estar firmados correctamente por una CA de confianza.

## <a name="resources"></a>Recursos

-   [Controladores de firma](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 
