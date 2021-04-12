---
description: Para ayudar a mantener la seguridad de una instalación de software, siga estas instrucciones al crear una Windows Installer acción personalizada.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Directrices para proteger las acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277555"
---
# <a name="guidelines-for-securing-custom-actions"></a>Directrices para proteger las acciones personalizadas

El cumplimiento de las siguientes directrices al crear un paquete de Windows Installer con acciones personalizadas ayuda a mantener un entorno seguro durante la instalación:

-   Proteja los archivos adicionales escritos por la acción personalizada.
-   Compruebe la longitud del búfer y la validez de todos los datos leídos por la acción personalizada. Esto incluye propiedades que pueden proporcionar datos a la acción personalizada, especialmente las que usan propiedades públicas proporcionadas por un usuario.
-   No confíe en archivos dll externos que no sean de confianza para el sistema en todas las plataformas en las que el paquete de instalación está diseñado para ejecutarse.
-   Considere detenidamente si desea usar acciones personalizadas que usen privilegios [*elevados*](e-gly.md) o suplantación. Acciones personalizadas como "abrir una dirección URL después de completarse la instalación", "iniciar el software después de completarse la instalación" o "iniciar el archivo Léame una vez completada la instalación" no suele requerir privilegios elevados para funcionar. Si la acción personalizada se debe ejecutar con privilegios *elevados* , asegúrese de que el código de acción personalizada se protege contra las saturaciones del búfer y la carga involuntaria de código no seguro. Tenga en cuenta que durante la fase de ejecución de la instalación, el instalador pasa información a un proceso con privilegios *elevados* y ejecuta el script. Cualquier acción personalizada que se ejecute durante la fase de ejecución puede ejecutarse con privilegios *elevados* .
-   Recopile toda la información proporcionada por el usuario durante la secuencia de IU. No solicite al usuario ninguna información que no se pueda establecer mediante una propiedad pública.
-   Si la acción personalizada de script expande propiedades, tome precauciones para asegurarse de que la acción personalizada está protegida contra la posibilidad de que se produzca la inyección de script. El script puede estar registrado en texto no cifrado.

Vea también [seguridad de la acción personalizada](custom-action-security.md).

 

 



