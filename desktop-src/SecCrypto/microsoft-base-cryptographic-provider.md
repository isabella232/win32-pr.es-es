---
description: El proveedor criptográfico base de Microsoft es el proveedor de servicios criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de CryptoAPI. Es un proveedor de uso general que admite firmas digitales y cifrado de datos.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Proveedor criptográfico base de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244071"
---
# <a name="microsoft-base-cryptographic-provider"></a>Proveedor criptográfico base de Microsoft

El proveedor criptográfico base de Microsoft es el proveedor de [*servicios*](../secgloss/c-gly.md) criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de [*CryptoAPI.*](../secgloss/c-gly.md) Es un proveedor de uso general que admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de datos.

El algoritmo de clave pública RSA se usa para todas las operaciones de clave pública.

Para mantener la compatibilidad con versiones anteriores, la nueva versión del proveedor conserva la designación de la versión 1.0 del nombre en Wincrypt.h. Sin embargo, la versión 2.0 de este proveedor se está enviando actualmente. Para determinar la versión real del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **PP \_ VERSION**. Si 0x0200 se devuelve en *pbData*, tiene la versión 2.0.

|                   | Value            |
|-------------------|------------------|
| **Tipo de proveedor** | PROV \_ RSA \_ FULL  |
| **Nombre del proveedor** | MS \_ DEF \_ PROV    |



 

 

 
