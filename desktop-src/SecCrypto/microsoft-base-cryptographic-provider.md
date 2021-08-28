---
description: El proveedor criptográfico base de Microsoft es el proveedor de servicios criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de CryptoAPI. Es un proveedor de uso general que admite firmas digitales y cifrado de datos.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Proveedor criptográfico base de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32082fc6cd7ec6d34bd994e3d3122e2b4c06eee290af8074cea0c183e5dd0116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100705"
---
# <a name="microsoft-base-cryptographic-provider"></a>Proveedor criptográfico base de Microsoft

El proveedor criptográfico base de Microsoft es el proveedor de [*servicios*](../secgloss/c-gly.md) criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de [*CryptoAPI.*](../secgloss/c-gly.md) Es un proveedor de uso general que admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de datos.

El algoritmo de clave pública RSA se usa para todas las operaciones de clave pública.

Para mantener la compatibilidad con versiones anteriores, la nueva versión del proveedor conserva la designación de la versión 1.0 del nombre en Wincrypt.h. Sin embargo, la versión 2.0 de este proveedor se está enviando actualmente. Para determinar la versión real del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **PP \_ VERSION**. Si 0x0200 se devuelve en *pbData*, tiene la versión 2.0.

|                   | Value            |
|-------------------|------------------|
| **Tipo de proveedor** | PROV \_ RSA \_ FULL  |
| **Nombre del proveedor** | MS \_ DEF \_ PROV    |



 

 

 
