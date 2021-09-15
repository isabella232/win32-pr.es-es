---
description: Contiene información que debe identificar de forma única al individuo que realiza la solicitud.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Campos de nombre distintivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a03495d19608e29aa60f09954c96a10f6c3cde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476483"
---
# <a name="distinguished-name-fields"></a>Campos de nombre distintivo

Una [*solicitud de certificado*](../secgloss/c-gly.md) contiene información que debe identificar de forma única al individuo que realiza la solicitud.

Las solicitudes de certificado con formato PKCS 10 aceptadas por Servicios de certificados contienen campos de identificación a los que se hace referencia como campos de nombre \# distintivo (DN). Estos campos contendrán la información que el usuario introduce cuando key manager, el [control](certificate-enrollment-control.md)de inscripción de certificados u otros medios crean una solicitud de certificado.

Estas son algunas directrices para la finalización de campos DN en una solicitud de certificado.



| Campo               | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre común         | Certificados de usuario: debe escribir el nombre completo de la persona. Certificados de equipo: debe escribir la ruta de acceso completa hostName* que se usa en las búsquedas DNS en las que se va a ejecutar el ***/**  servidor (por ejemplo, *HostName*. _Ejemplo_* _.com_*).<br/>                                                                                                  |
| Organización        | El nombre que especifique para el campo Organización debe ser el nombre legal de la organización que esté registrada con la autoridad de ciudad, estado o país o región correspondiente. El nombre legal de la organización debe usarse en el campo Organización.                                                                                                      |
| Unidad organizativa | El campo Unidad organizativa se puede usar para diferenciar entre diferentes divisiones dentro de una organización, por ejemplo, "Unidad de seguridad de Internet" o "Recursos humanos". También se recomienda usar este campo para especificar un valor DBA (Doing Business As...).                                                                                           |
| Localidad            | El campo Localidad indica la ciudad en la que reside la organización. Si la organización solo tiene una posición local, en virtud de tener una licencia comercial registrada con el empleado de city para la ciudad de Catalina en el estado de Massachusetts, el campo Localidad debe contener Catalina.                                                                |
| Estado o provincia   | El campo Estado o Provincia especifica dónde se encuentra físicamente la organización. Si su organización se incorpora en Asíncro, pero tiene un DBA (Doing Business As...) en California, use California. El campo Estado o Provincia no debe ser un campo abreviado. Por ejemplo, "CA" no es un nombre de estado válido. "California" es el nombre de estado adecuado. |
| País/región      | El [*estándar X.500*](../secgloss/x-gly.md) Naming Scheme requiere un código de país o región de 2 caracteres. El código de país o región de la Estados Unidos es EE. UU.; el código de país o región de Canadá es CA.                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de nombre](name-properties.md)
</dt> </dl>

 

 
