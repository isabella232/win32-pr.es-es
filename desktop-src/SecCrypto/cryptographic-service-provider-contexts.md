---
description: La primera función cryptoAPI a la que llama una aplicación que usa cualquier API criptográfica es la función CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contextos del proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ad2e77178ade8cc286dae1ff7334c89d33e46a63af227503f8e163f7d81cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768637"
---
# <a name="cryptographic-service-provider-contexts"></a>Contextos del proveedor de servicios criptográficos

La primera [*función cryptoAPI*](../secgloss/c-gly.md) a la que llama una aplicación que usa cualquier API criptográfica es [**la función CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) Esta función devuelve un identificador a un CSP determinado que incluye la especificación de un contenedor [*de claves determinado*](../secgloss/k-gly.md) dentro del CSP. Este contenedor de claves es un contenedor de claves solicitado específicamente o es el contenedor de claves predeterminado para el usuario que ha iniciado sesión actualmente.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) también puede crear un nuevo contenedor de claves. Para obtener más información, vea Ejemplo de [programa C: Creación](example-c-program-creating-a-key-container-and-generating-keys.md) de un contenedor de claves y Generación de claves y Programa C de [ejemplo: Uso de CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) tiene un nombre y un tipo. Por ejemplo, el nombre de uno de los CSP incluidos actualmente con el sistema operativo es [Proveedor criptográfico base de Microsoft](microsoft-base-cryptographic-provider.md). Es un proveedor [de tipo \_ PROV RSA \_ FULL.](prov-rsa-full.md) El nombre de cada proveedor es único; el tipo de proveedor no es .

Cuando una aplicación llama a [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obtener un identificador de CSP, especifica un tipo de proveedor y, opcionalmente, un nombre de proveedor. Si se especifican un tipo y un nombre, la función carga el CSP con el tipo de proveedor y el nombre del proveedor correspondientes. La función devuelve el identificador del CSP, que proporciona acceso al CSP y a un contenedor [*de claves*](../secgloss/k-gly.md) dentro del CSP.

Cuando una aplicación llama a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) y especifica un tipo de proveedor pero ningún nombre de proveedor, la función busca un proveedor con nombre, comprobando primero una lista de proveedores con nombre predeterminados asociados al usuario que inició sesión y, si se produce un error, en una lista de proveedores con nombre predeterminados asociados al equipo. Una vez determinado el nombre del proveedor, la función **CryptAcquireContext** busca el CSP para ese proveedor, lo carga y devuelve su identificador.

Cuando haya terminado de usar un identificador de CSP, descríbalo llamando a la [**función CryptReleaseContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

 

 
