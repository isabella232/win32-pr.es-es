---
description: El proveedor de servicios criptográficos básicos de Microsoft es el proveedor de proveedores de servicios criptográficos (CSP) inicial y se distribuye con las versiones de CryptoAPI 1,0 y 2,0. Es un proveedor de uso general que admite firmas digitales y cifrado de datos.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Proveedor de servicios criptográficos básicos de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686866"
---
# <a name="microsoft-base-cryptographic-provider"></a>Proveedor de servicios criptográficos básicos de Microsoft

El proveedor de servicios criptográficos básicos de Microsoft es el proveedor de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) (CSP) inicial y se distribuye con las versiones de [*CryptoAPI*](../secgloss/c-gly.md) 1,0 y 2,0. Es un proveedor de uso general que admite [*firmas digitales*](../secgloss/d-gly.md) y cifrado de datos.

El algoritmo de clave pública RSA se utiliza para todas las operaciones de clave pública.

Para mantener la compatibilidad con versiones anteriores con versiones anteriores, la nueva versión del proveedor conserva la designación de la versión 1,0 del nombre en Wincrypt. h. Sin embargo, la versión 2,0 de este proveedor se está distribuyendo actualmente. Para determinar la versión real del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **la \_ versión PP**. Si 0x0200 se devuelve en *pbData*, tendrá la versión 2,0.

|                |                     |
|----------------|---------------------|
| Tipo de proveedor: | **aprovisionamiento \_ completo de RSA \_** |
| Nombre del proveedor: | **Prov de MS \_ Def \_**   |



 

 

 
