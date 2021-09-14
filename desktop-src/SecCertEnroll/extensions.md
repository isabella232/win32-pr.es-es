---
description: El formato de certificado X.509 versión 3 identifica varias extensiones que se pueden agregar a un certificado.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensiones (API de inscripción de certificados)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069039"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensiones (API de inscripción de certificados)

El formato de certificado X.509 versión 3 identifica varias extensiones que se pueden agregar a un certificado. Las extensiones proporcionan información mejorada sobre el uso de claves, las directivas y restricciones de certificados, los formularios de nombres alternativos, etc. Puede usar la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir un valor de extensión. Muchas de las extensiones comunes se pueden crear mediante interfaces predefinidas derivadas de **IX509Extension**. Se agrega una colección de extensiones a una solicitud de certificado mediante la inclusión de la colección en los atributos de solicitud. Para obtener más información, vea los temas siguientes:

-   [Extensiones admitidas](supported-extensions.md)
-   [Extensiones PKCS \# 10](pkcs--10-extensions.md)
-   [Extensiones de CMC](cmc-extensions.md)

 

 



