---
title: Protección de credenciales y aplicaciones de terceros
description: Credential Guard no permite que SSP de terceros soliciten hashes de contraseña de LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467137"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Proveedores de soporte técnico de seguridad de terceros con Credential Guard

Credential Guard no permite que SSP de terceros soliciten hashes de contraseña de LSA. Sin embargo, los SSP y puntos de acceso personalizados siguen recibiendo la notificación de la contraseña cuando un usuario inicia sesión o cambia su contraseña. No se admite el uso de API no documentadas dentro de los SSP y puntos de acceso personalizados.

Cuando la amplitud y profundidad de las protecciones que ofrece Credential Guard aumentan, las versiones posteriores de Windows 10 que ejecuten Credential Guard podrían influir en los escenarios que estaban funcionando en el pasado. Por ejemplo, Credential Guard puede bloquear el uso de un tipo determinado de credencial o un componente determinado para evitar que el malware aproveche las vulnerabilidades. Por lo tanto, te recomendamos que los escenarios necesarios para las operaciones de una organización se prueben antes de actualizar un dispositivo que con Credential Guard en ejecución.

Consulte este artículo [para obtener la](/windows/security/identity-protection/credential-guard/credential-guard) descripción completa y las mitigaciones recomendadas.

 

 