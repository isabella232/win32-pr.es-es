---
description: Curvas elípticas habilitadas en las versiones 1507 y 1511 de Windows 10.
title: Curvas elípticas de TLS en Windows 10, versión 1507 y 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720656"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>Curvas elípticas de TLS en Windows 10, versión 1507 y 1511

En el caso de las versiones 1507 y 1511 de Windows 10, las siguientes curvas elípticas están habilitadas y en este orden de prioridad de forma predeterminada con el proveedor de Microsoft Schannel:

| Cadena de curva elíptica | Disponible en modo FIPS |
|-------------|--------------|
| NistP256 | Sí |
| NistP384 | Sí |


El proveedor de Microsoft Schannel admite las siguientes curvas elípticas, pero no está habilitada de forma predeterminada:

| Cadena de curva elíptica | Disponible en modo FIPS |
|-------------|--------------|
| brainpoolP256r1 | No |
| brainpoolP384r1 | No |
| brainpoolP512r1 | No |
| nistP192 | No |
| nistP224 | No |
| nistP521 | Sí |
| secP160k1 | No |
| secP160r1 | No |
| secP160r2 | No |
| secP192k1 | No |
| secP192r1 | No |
| secP224k1 | No |
| secP224r1 | No |
| secP256k1 | No |
| secP256r1 | No |
| secP384r1 | No |
| secP521r1 | No |

## <a name="enabling-elliptic-curves"></a>Habilitar curvas elípticas

Para agregar curvas elípticas, implemente una directiva de grupo o use los cmdlets de TLS:
- Para usar la Directiva de grupo, [Configure el orden de las curvas ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) en configuración del equipo > plantillas administrativas > de red > configuración de SSL con la lista de prioridades para todas las curvas elípticas que desee habilitar.

- Para usar PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obtener una lista completa de la sintaxis y las descripciones de los cmdlets de TLS.


> [!NOTE]
> Antes de Windows 10, las cadenas de conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite un valor de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la Directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.


## <a name="see-also"></a>Consulte también

[Configuración del orden de las curvas ECC de TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Administrar el orden ECC de TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Administrar curvas ECC de Windows mediante directiva de grupo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlets de TLS](/powershell/module/tls)
