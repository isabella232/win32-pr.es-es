---
description: Los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios. Los proveedores se pueden implementar en hardware, software o ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Descripción de los proveedores de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002524"
---
# <a name="understanding-cryptographic-providers"></a>Descripción de los proveedores de servicios criptográficos

El concepto de proveedor de servicios criptográficos que se presentó en Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) y que evolucionó en cierto modo en [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) es fundamental para la implementación segura de la funcionalidad criptográfica en los sistemas operativos de Microsoft. Estos dos SDK se han usado para crear muchas aplicaciones y otros SDK las llaman internamente. Por ejemplo, Active Directory servicios de Certificate Server y la API de inscripción de certificados se basan en CryptoAPI y CNG.

En general, los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios. Los proveedores se pueden implementar en hardware, software o ambos. Las aplicaciones compiladas con CryptoAPI o CNG no pueden modificar las claves creadas por los proveedores y no pueden modificar la implementación de algoritmos criptográficos. Los diversos proveedores creados por Microsoft se distribuyen con los sistemas operativos. Otros proveedores se han creado y distribuido por terceros.

En los temas siguientes se resaltan las diferencias entre los proveedores asociados con CryptoAPI y los asociados a CNG. Normalmente, esta documentación hace referencia a los proveedores sin referencia al SDK con el que están asociados, anotando la Asociación solo cuando es relevante.

-   [Proveedores de servicios criptográficos de CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Proveedores de algoritmos criptográficos CNG](cng-cryptographic-algorithm-providers.md)
-   [Proveedores de almacenamiento de claves CNG](cng-key-storage-providers.md)
-   [Enumerar los proveedores instalados](enumerating-installed-providers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
