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
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706755"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Proveedores de soporte técnico de seguridad de terceros con Credential Guard

Credential Guard no permite que SSP de terceros soliciten hashes de contraseña de LSA. Sin embargo, los SSP y puntos de acceso personalizados siguen recibiendo la notificación de la contraseña cuando un usuario inicia sesión o cambia su contraseña. No se admite el uso de API no documentadas dentro de los SSP y puntos de acceso personalizados.

Cuando la amplitud y profundidad de las protecciones que ofrece Credential Guard aumentan, las versiones posteriores de Windows 10 que ejecuten Credential Guard podrían influir en los escenarios que estaban funcionando en el pasado. Por ejemplo, Credential Guard puede bloquear el uso de un tipo determinado de credencial o un componente determinado para evitar que el malware aproveche las vulnerabilidades. Por lo tanto, te recomendamos que los escenarios necesarios para las operaciones de una organización se prueben antes de actualizar un dispositivo que con Credential Guard en ejecución.

Consulte este artículo [para obtener la](/windows/security/identity-protection/credential-guard/credential-guard) descripción completa y las mitigaciones recomendadas.

 

 