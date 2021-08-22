---
description: Para ayudar a mantener una instalación de software segura, siga estas directrices al crear una Windows personalizada del instalador.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Directrices para proteger acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b5ea12bd8d38025587cb09fd7a17d3e87739acedf31d85f72ff4b1b76b0432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649295"
---
# <a name="guidelines-for-securing-custom-actions"></a>Directrices para proteger acciones personalizadas

El cumplimiento de las siguientes directrices al crear un paquete Windows Installer con acciones personalizadas ayuda a mantener un entorno seguro durante la instalación:

-   Proteja los archivos adicionales escritos por la acción personalizada.
-   Compruebe las longitudes del búfer y la validez de todos los datos leídos por la acción personalizada. Esto incluye las propiedades que pueden proporcionar datos a la acción personalizada, especialmente aquellas que usan propiedades públicas proporcionadas por un usuario.
-   No se base en archivos DLL externos que no sean de confianza para el sistema en todas las plataformas en las que se va a ejecutar el paquete de instalación.
-   Considere detenidamente si se deben usar acciones personalizadas que [*usen*](e-gly.md) privilegios elevados o suplantación. Las acciones personalizadas, como "abrir una dirección URL una vez completada la instalación", "iniciar el software una vez completada la instalación" o "iniciar Léame una vez completada la instalación", normalmente no requerirían privilegios elevados para funcionar. Si la acción personalizada  debe ejecutarse con privilegios elevados, asegúrese de que el código de acción personalizada se protege contra saturaciones del búfer y la carga involuntaria de código no seguro. Tenga en cuenta que durante la fase de ejecución de  la instalación, el instalador pasa información a un proceso con privilegios elevados y ejecuta el script. Las acciones personalizadas que se ejecutan durante la fase de ejecución pueden ejecutarse con *privilegios* elevados.
-   Recopila toda la información proporcionada por el usuario durante la secuencia de la interfaz de usuario. No solicite al usuario ninguna información que no se pueda establecer mediante una propiedad pública.
-   Si la acción personalizada del script expande las propiedades, tome precauciones de que la acción personalizada está protegida contra la posibilidad de inyección de scripts. El script se puede registrar en texto sin formato.

Consulte también Seguridad [de acción personalizada.](custom-action-security.md)

 

 



