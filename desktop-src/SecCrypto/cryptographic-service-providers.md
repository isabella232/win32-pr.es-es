---
description: 'Importante: esta API está en desuso.'
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Proveedores de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423776"
---
# <a name="cryptographic-service-providers"></a>Proveedores de servicios criptográficos

> [!IMPORTANT]
> Esta API está en desuso. El software nuevo y existente debe empezar a usar las [API de Cryptography Next Generation.](/windows/desktop/SecCNG/cng-portal) Microsoft puede quitar esta API en futuras versiones.

 

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) contiene implementaciones de algoritmos y estándares criptográficos. Como mínimo, un CSP consta de una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll) que implementa las funciones de [*CryptoSPI*](../secgloss/c-gly.md) (una [*interfaz de programa del sistema*](../secgloss/s-gly.md)). La mayoría de los CSP contienen la implementación de todas sus propias funciones. Sin embargo, algunos CSP implementan sus funciones principalmente en un programa de servicio basado en Windows administrado por el administrador de control de servicios de Windows. Otros implementan funciones en hardware, como una [*tarjeta inteligente*](../secgloss/s-gly.md) o un coprocesador seguro. Si un CSP no implementa sus propias funciones, el archivo DLL actúa como capa de paso a través, lo que facilita la comunicación entre el sistema operativo y la implementación de CSP real.

Esta sección incluye los temas siguientes.



| Tema                                                                                      | Contenido                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md)                           | Los tipos de proveedor de servicios criptográficos son familias de proveedores de servicios de cifrado que comparten formatos de datos y protocolos criptográficos. Los formatos de datos incluyen esquemas de [*relleno*](../secgloss/p-gly.md) de algoritmos, [*longitudes de clave*](../secgloss/k-gly.md)y modos predeterminados. |
| [Proveedores de servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md) | Información detallada sobre los CSP disponibles actualmente en Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
