---
description: Curvas elípticas habilitadas Windows 10 versión 1607 y posteriores.
title: Curvas elípticas TLS Windows 10 versión 1607 y posteriores
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 237d0f7a7b4b2a7fecb99a91f21c55349e7d435b221e1b3297afd1ba614cc92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915850"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Curvas elípticas TLS Windows 10 versión 1607 y posteriores

Por Windows 10 versiones 1607 y posteriores, se habilitan las curvas elípticas siguientes y, de forma predeterminada, en este orden de prioridad mediante el proveedor de Microsoft Schannel:

| Cadena de curva elíptica | Disponible en modo FIPS |
|-------------|--------------|
| curve25519 | No |
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
- Para usar la directiva de grupo, configure el orden de curva [ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) en Configuración del equipo > Plantillas administrativas > Network > SSL Configuration Configuración con la lista de prioridad de todas las curvas elípticas que quiera habilitar.

- Para usar PowerShell, consulte [Cmdlets tls para](/powershell/module/tls) obtener una lista completa de la sintaxis y descripciones de los cmdlets TLS.


> [!NOTE]
> Antes de Windows 10, las cadenas del conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite una configuración de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.


## <a name="see-also"></a>Consulte también

[Configuración del orden de curva DE TLS ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Administración del pedido de TLS ECC](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Administración Windows curvas ECC mediante directiva de grupo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlets TLS](/powershell/module/tls)
