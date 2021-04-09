---
description: Cada propiedad de control de inscripción de certificado es de lectura/escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Uso de las propiedades de control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811227"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Uso de las propiedades de control de inscripción de certificados

Cada propiedad de control de inscripción de certificado es de lectura/escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables. Puede establecer una propiedad en cualquier valor de este conjunto para modificar el comportamiento de los métodos que usan la propiedad. Para obtener un comportamiento deseado, establezca la propiedad antes de llamar al método que utiliza el valor de la propiedad.

Sin embargo, tenga en cuenta que después de llamar a los métodos siguientes

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

las siguientes propiedades están bloqueadas para restablecerse

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**Especificación**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**ContainerName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

a menos que se llame al método [**ICEnroll4:: RESET**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) .

Para obtener información sobre las propiedades y los métodos individuales, vea los temas de referencia de esas propiedades y métodos en la [referencia de criptografía](cryptography-reference.md).

Las secciones siguientes contienen información específica del idioma para establecer y recuperar las propiedades del control de inscripción de certificados:

-   [Propiedades de control de inscripción de certificados en C++](certificate-enrollment-control-properties-in-c-.md)

 

 
