---
description: Sugerencias para las evaluaciones de seguridad de aplicaciones para el desarrollo de aplicaciones de software de seguridad de Windows y desarrollo de software seguro, incluidas las pruebas de seguridad de aplicaciones.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Prácticas recomendadas para las API de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669672"
---
# <a name="best-practices-for-the-security-apis"></a>Prácticas recomendadas para las API de seguridad

Para ayudar a desarrollar software seguro, se recomienda usar las siguientes prácticas recomendadas al desarrollar aplicaciones de. Para obtener más información, vea [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Ciclo de vida de desarrollo de seguridad

El [ciclo de vida de desarrollo de seguridad](/previous-versions/ms995349(v=msdn.10)) (SDL) es un proceso que alinea una serie de actividades y entregas orientadas a la seguridad en cada fase del desarrollo de software. Estas actividades y entregas incluyen:

-   Desarrollo de modelos de amenazas
-   Usar herramientas de exploración de código
-   Realización de revisiones de código y pruebas de seguridad

Para obtener más información acerca de SDL, consulte el [blog de SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelos de amenazas

La realización de un análisis del modelo de amenazas puede ayudarle a detectar posibles puntos de ataque en el código. Para obtener más información acerca del análisis del modelo de amenazas, consulte Howard, Michael y LeBlanc, David \[ 2003 \] , *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Es posible que este recurso no esté disponible en algunos idiomas y países).

## <a name="service-packs-and-security-updates"></a>Service Packs y actualizaciones de seguridad

Los entornos de compilación y prueba deben reflejar los mismos niveles de Service Pack y las actualizaciones de seguridad de la base de usuarios de destino. Le recomendamos que instale los Service Packs y las actualizaciones de seguridad más recientes para cualquier plataforma o aplicación de Microsoft que forme parte de su entorno de compilación y prueba, e anime a los usuarios a hacer lo mismo para el entorno de la aplicación finalizado. Para obtener más información acerca de los Service Pack y las actualizaciones de seguridad, consulte [microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) y [seguridad de Microsoft](https://www.microsoft.com/security).

## <a name="authorization"></a>Authorization

Debe crear aplicaciones que requieran el menor privilegio posible. El uso del menor privilegio posible reduce el riesgo de que el código malintencionado comprometa el sistema del equipo. Para obtener más información sobre cómo ejecutar el código en el menor nivel de privilegios posible, vea [ejecutar con privilegios especiales](running-with-special-privileges.md).

## <a name="more-information"></a>Más información

Para obtener más información acerca de los procedimientos recomendados, vea los temas siguientes.



| Tema                                                                                                                        | Descripción                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ejecutar con privilegios especiales](running-with-special-privileges.md)<br/>                                            | Describe las implicaciones de seguridad de los privilegios.<br/>                                                                                                                                  |
| [Evitar saturaciones del búfer](avoiding-buffer-overruns.md)<br/>                                                          | Proporciona información sobre cómo evitar las saturaciones del búfer.<br/>                                                                                                                            |
| [Protección de flujo de control (CFG) ](control-flow-guard.md)<br/>                                                                | Describe las vulnerabilidades de daños en la memoria.<br/>                                                                                                                                    |
| [Crear una DACL](creating-a-dacl.md)<br/>                                                                            | Muestra cómo crear una lista de control de acceso discrecional (DACL) mediante el [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).<br/> |
| [Administrar contraseñas](handling-passwords.md)<br/>                                                                      | Describe las implicaciones de seguridad del uso de contraseñas.<br/>                                                                                                                             |
| [Cómo optimizar la búsqueda de MSDN Library](how-to-optimize-your-msdn-library-search.md)<br/>                          | Describe las opciones para buscar contenido del SDK de seguridad en MSDN Library.<br/>                                                                                                           |
| [Extensibilidad del desarrollador de Access Control dinámico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientación básica a algunos de los puntos de extensibilidad de desarrollador para las nuevas soluciones de Access Control dinámicas.<br/>                                                                   |



 

 

