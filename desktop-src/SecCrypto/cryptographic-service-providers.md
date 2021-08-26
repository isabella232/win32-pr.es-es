---
description: Importante Esta API está en desuso.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Proveedores de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7ef58122e47594b195700241b936b8985cd88137c52841976495b195d7e4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876195"
---
# <a name="cryptographic-service-providers"></a>Proveedores de servicios criptográficos

> [!IMPORTANT]
> Esta API está en desuso. El software nuevo y existente debe empezar a [usar Cryptography Next Generation API.](/windows/desktop/SecCNG/cng-portal) Microsoft puede quitar esta API en futuras versiones.

 

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) contiene implementaciones de estándares y algoritmos criptográficos. Como mínimo, un CSP consta [](../secgloss/d-gly.md) de una biblioteca de vínculos dinámicos (DLL) que implementa las funciones de [*CryptoSPI*](../secgloss/c-gly.md) (una interfaz [*de programa del sistema*](../secgloss/s-gly.md)). La mayoría de los CSP contienen la implementación de todas sus propias funciones. Sin embargo, algunos PROVEEDORES de servicios implementan sus funciones principalmente en un programa de servicio basado en Windows administrado por el Windows de control de servicios. Otros implementan funciones en hardware, como una [*tarjeta inteligente o*](../secgloss/s-gly.md) un coprocesador seguro. Si un CSP no implementa sus propias funciones, el archivo DLL actúa como una capa de paso a través, lo que facilita la comunicación entre el sistema operativo y la implementación de CSP real.

Esta sección incluye los temas siguientes.



| Tema                                                                                      | Contenido                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md)                           | Los tipos de proveedores criptográficos son familias de proveedores de servicios criptográficos que comparten formatos de datos y protocolos criptográficos. Los formatos de datos [*incluyen*](../secgloss/p-gly.md) esquemas de relleno de algoritmos, [*longitudes de clave*](../secgloss/k-gly.md)y modos predeterminados. |
| [Proveedores de servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md) | Información detallada sobre los CSP disponibles actualmente en Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
