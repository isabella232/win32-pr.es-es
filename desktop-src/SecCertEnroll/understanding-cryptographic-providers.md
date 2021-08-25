---
description: Los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios. Los proveedores se pueden implementar en hardware, software o ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Descripción de los proveedores criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f167f186ed4da1ac5e97aba8a3c4659f13f29f253de3f489981fc6b32810015f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127225"
---
# <a name="understanding-cryptographic-providers"></a>Descripción de los proveedores criptográficos

El concepto de proveedor criptográfico que se introdujo en Cryptography API [*(CryptoAPI)*](/windows/desktop/SecGloss/c-gly)y que evolucionó ligeramente en [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) es fundamental para la implementación segura de la funcionalidad criptográfica en sistemas operativos de Microsoft. Estos dos SDK se han usado para crear muchas aplicaciones y otros SDK los llaman internamente. Por ejemplo, Servicios de certificados de Active Directory api de inscripción de certificados se basan en CryptoAPI y CNG.

En general, los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios. Los proveedores se pueden implementar en hardware, software o ambos. Las aplicaciones creadas mediante CryptoAPI o CNG no pueden modificar las claves creadas por los proveedores y no pueden modificar la implementación de algoritmos criptográficos. Los varios proveedores creados por Microsoft se distribuyen con los sistemas operativos. Otros proveedores han sido creados y distribuidos por terceros.

En los temas siguientes se resaltan las diferencias entre los proveedores asociados a CryptoAPI y los asociados a CNG. Normalmente, esta documentación hace referencia a proveedores sin referencia al SDK al que están asociados, y se indica la asociación solo cuando es pertinente.

-   [Proveedores de servicios criptográficos CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Proveedores de algoritmos criptográficos CNG](cng-cryptographic-algorithm-providers.md)
-   [Proveedores de claves Storage CNG](cng-key-storage-providers.md)
-   [Enumeración de proveedores instalados](enumerating-installed-providers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
