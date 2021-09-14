---
description: Para ayudar a mantener una instalación de software segura, siga estas instrucciones al crear una Windows personalizada del instalador.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Directrices para proteger acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074716"
---
# <a name="guidelines-for-securing-custom-actions"></a>Directrices para proteger acciones personalizadas

El cumplimiento de las siguientes directrices al crear un paquete Windows Installer con acciones personalizadas ayuda a mantener un entorno seguro durante la instalación:

-   Proteja los archivos adicionales escritos por la acción personalizada.
-   Compruebe la longitud del búfer y la validez de todos los datos leídos por la acción personalizada. Esto incluye las propiedades que pueden proporcionar datos a la acción personalizada, especialmente aquellas que usan propiedades públicas proporcionadas por un usuario.
-   No se base en archivos DLL externos que no sean de confianza para el sistema en todas las plataformas en las que se va a ejecutar el paquete de instalación.
-   Considere detenidamente si se deben usar acciones personalizadas que usen [*privilegios*](e-gly.md) elevados o suplantación. Las acciones personalizadas como "abrir una dirección URL una vez completada la instalación", "iniciar el software una vez completada la instalación" o "iniciar Léame una vez completada la instalación" no suelen requerir privilegios elevados para funcionar. Si la acción personalizada  debe ejecutarse con privilegios elevados, asegúrese de que el código de acción personalizada protege contra las saturaciones del búfer y la carga involuntaria de código no seguro. Tenga en cuenta que durante la fase de ejecución de  la instalación, el instalador pasa información a un proceso con privilegios elevados y ejecuta el script. Las acciones personalizadas que se ejecutan durante la fase de ejecución pueden ejecutarse con *privilegios* elevados.
-   Recopila toda la información proporcionada por el usuario durante la secuencia de la interfaz de usuario. No solicite al usuario ninguna información que no se pueda establecer mediante una propiedad pública.
-   Si la acción personalizada del script expande las propiedades, tome precauciones de que la acción personalizada está protegida frente a la posibilidad de inyección de scripts. El script se puede registrar en texto no especificado.

Consulte también [Seguridad de acciones personalizadas.](custom-action-security.md)

 

 



