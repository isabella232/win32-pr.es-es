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
ms.openlocfilehash: 534c3cf9268f21c36d982a627de2e1b293ffdca1e1fd4ffc2acd0db9f7d6059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867945"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensiones (API de inscripción de certificados)

El formato de certificado X.509 versión 3 identifica varias extensiones que se pueden agregar a un certificado. Las extensiones proporcionan información mejorada sobre el uso de claves, las directivas de certificado y las restricciones, los formularios de nombre alternativos, etc. Puede usar la [**interfaz IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir un valor de extensión. Muchas de las extensiones comunes se pueden crear mediante interfaces predefinidas derivadas de **IX509Extension**. Se agrega una colección de extensiones a una solicitud de certificado mediante la inclusión de la colección en los atributos de solicitud. Para obtener más información, vea los temas siguientes:

-   [Extensiones admitidas](supported-extensions.md)
-   [Extensiones PKCS \# 10](pkcs--10-extensions.md)
-   [Extensiones de CMC](cmc-extensions.md)

 

 



