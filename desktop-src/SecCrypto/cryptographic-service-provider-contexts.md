---
description: La primera función CryptoAPI llamada por una aplicación que usa cualquier API criptográfica es la función CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contextos de proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df20df528b0ba0c385c7ab690436351d918f1521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154087"
---
# <a name="cryptographic-service-provider-contexts"></a>Contextos de proveedor de servicios criptográficos

La primera función [*CryptoAPI*](../secgloss/c-gly.md) llamada por una aplicación que usa cualquier API criptográfica es la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) . Esta función devuelve un identificador a un CSP determinado que incluye la especificación de un [*contenedor de claves*](../secgloss/k-gly.md) determinado dentro del CSP. Este contenedor de claves es un contenedor de claves solicitado específicamente o es el contenedor de claves predeterminado para el usuario que ha iniciado sesión actualmente.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) también puede crear un nuevo contenedor de claves. Para obtener más información, vea [el ejemplo c programa: crear un contenedor de claves y generar claves](example-c-program-creating-a-key-container-and-generating-keys.md) y [programa c de ejemplo: uso de CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) tiene un nombre y un tipo. Por ejemplo, el nombre de uno de los CSP incluidos actualmente con el sistema operativo es [proveedor de servicios criptográficos básicos de Microsoft](microsoft-base-cryptographic-provider.md). Es un proveedor de tipo [ \_ \_ completo de Prov RSA](prov-rsa-full.md) . El nombre de cada proveedor es único; el tipo de proveedor no es.

Cuando una aplicación llama a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador de CSP, especifica un tipo de proveedor y, opcionalmente, un nombre de proveedor. Si se especifican un tipo y un nombre, la función carga el CSP con el tipo de proveedor y el nombre de proveedor coincidentes. La función devuelve el identificador del CSP que proporciona acceso al CSP y a un contenedor de [*claves*](../secgloss/k-gly.md) dentro del CSP.

Cuando una aplicación llama a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) y especifica un tipo de proveedor pero ningún nombre de proveedor, la función busca un proveedor con nombre, comprobando primero una lista de proveedores con nombre predeterminados asociados al usuario que ha iniciado sesión y, si se produce un error, de una lista de proveedores con nombre predeterminados asociados al equipo. Una vez determinado el nombre del proveedor, la función **CryptAcquireContext** busca el CSP para ese proveedor, lo carga y devuelve su identificador.

Cuando haya terminado de usar un identificador de CSP, suéltelo llamando a la función [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) .

 

 
