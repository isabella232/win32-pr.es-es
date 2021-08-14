---
description: Curvas elípticas habilitadas Windows 10 versiones 1507 y 1511.
title: Curvas elípticas TLS Windows 10 1507 y 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 91dfc7dac8f45b9c4f2231f6db93e776c75544373199170146f55362f02f2be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915870"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>Curvas elípticas TLS Windows 10 1507 y 1511

Por Windows 10, las versiones 1507 y 1511, se habilitan las siguientes curvas elípticas y, de forma predeterminada, en este orden de prioridad mediante el proveedor de Microsoft Schannel:

| Cadena de curva elíptica | Disponible en modo FIPS |
|-------------|--------------|
| NistP256 | Sí |
| NistP384 | Sí |


Las siguientes curvas elípticas son compatibles con el proveedor de Microsoft Schannel, pero no están habilitadas de forma predeterminada:

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

## <a name="enabling-elliptic-curves"></a>Habilitación de curvas elípticas

Para agregar curvas elípticas, implemente una directiva de grupo o use los cmdlets TLS:
- Para usar la directiva de grupo, configure ecc curve order (Orden de curva [ecc)](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) en Configuración del equipo > Plantillas administrativas > Network > SSL Configuration Configuración con la lista de prioridad de todas las curvas elípticas que quiera habilitar.

- Para usar PowerShell, consulte [Cmdlets tls para](/powershell/module/tls) obtener una lista completa de la sintaxis y descripciones de los cmdlets TLS.


> [!NOTE]
> Antes de Windows 10, las cadenas del conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite una configuración de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.


## <a name="see-also"></a>Consulte también

[Configuración del orden de curva DE TLS ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Administración del pedido de TLS ECC](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Administración Windows curvas ECC mediante directiva de grupo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlets TLS](/powershell/module/tls)
