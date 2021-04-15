---
description: Contiene información que debe identificar de forma única a la persona que realiza la solicitud.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Campos de nombre distintivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a03495d19608e29aa60f09954c96a10f6c3cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545470"
---
# <a name="distinguished-name-fields"></a>Campos de nombre distintivo

Una [*solicitud de certificado*](../secgloss/c-gly.md) contiene información que debe identificar de forma única a la persona que realiza la solicitud.

\#Las solicitudes de certificado de formato PKCS 10 que son aceptadas por los servicios de Certificate Server contienen campos de identificación a los que se hace referencia como campos de nombre distintivo (DN). Estos campos contendrán la información que proporciona el usuario cuando se crea una solicitud de certificado mediante el administrador de claves, el [control de inscripción de certificados](certificate-enrollment-control.md)o algún otro medio.

A continuación se indican algunas instrucciones para completar los campos DN en una solicitud de certificado.



| Campo               | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre común         | Certificados de usuario: debe escribir el nombre completo de la persona. Certificados de equipo: debe especificar la ruta de *acceso completa del nombre de host * **/**  que se usa en las búsquedas de DNS en las que se ejecutará el servidor (por ejemplo, *nombre de host ***.** _Ejemplo_* de _. com_*).<br/>                                                                                                  |
| Organización        | El nombre que especifique para el campo organización debe ser el nombre legal de la organización registrado con la ciudad, el estado o la autoridad de país o región adecuados. El nombre legal de la organización debe usarse en el campo organización.                                                                                                      |
| Unidad organizativa | El campo unidad organizativa se puede utilizar para diferenciar entre distintas divisiones de una organización, por ejemplo, "unidad de seguridad de Internet" o "recursos humanos". También se recomienda usar este campo para especificar un valor de DBA (hacer negocios como...).                                                                                           |
| Localidad            | El campo localidad indica la ciudad en la que reside la organización. Si la organización solo tiene que tener en cuenta la ciudad de Cambridge en el estado de Massachusetts, en virtud de tener una licencia empresarial registrada con el responsable de la ciudad de Cambridge, el campo local debe contener Cambridge.                                                                |
| Estado o provincia   | El campo Estado o provincia especifica dónde se encuentra físicamente la organización. Si su organización está incorporada en Delaware pero tiene un DBA (hacer negocios como...) en California, use California. El campo de estado o provincia no debe ser un campo abreviado. Por ejemplo, "CA" no es un nombre de estado válido. "California" es el nombre de estado adecuado. |
| País/región      | El estándar de esquema de nombres [*X. 500*](../secgloss/x-gly.md) requiere un código de país o región de dos caracteres. El código de país o región para la Estados Unidos es US; el código de país o región para Canadá es CA.                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de nombre](name-properties.md)
</dt> </dl>

 

 
