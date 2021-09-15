---
description: Cada propiedad control de inscripción de certificados es de lectura y escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Uso de las propiedades del control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127477648"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Uso de las propiedades del control de inscripción de certificados

Cada propiedad control de inscripción de certificados es de lectura y escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables. Puede establecer una propiedad en cualquier valor dentro de este conjunto para modificar el comportamiento de los métodos que usan la propiedad . Para obtener un comportamiento deseado, establezca la propiedad antes de llamar al método que usa el valor de esa propiedad.

Sin embargo, tenga en cuenta que después de llamar a los métodos siguientes

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

se bloquea el restablecimiento de las siguientes propiedades

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**ContainerName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

a menos que se llame al método [**ICEnroll4::Reset.**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset)

Para obtener información sobre propiedades y métodos individuales, vea los temas de referencia de esas propiedades y métodos en [la Referencia de criptografía](cryptography-reference.md).

Las secciones siguientes contienen información específica del idioma para establecer y recuperar las propiedades del control de inscripción de certificados:

-   [Propiedades del control de inscripción de certificados en C++](certificate-enrollment-control-properties-in-c-.md)

 

 
