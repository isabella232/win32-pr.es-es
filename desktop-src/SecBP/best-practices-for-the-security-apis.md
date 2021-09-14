---
description: Sugerencias para las evaluaciones de seguridad de aplicaciones para el desarrollo de aplicaciones Windows software de seguridad y desarrollo de software seguro, incluidas las pruebas de seguridad de aplicaciones.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Procedimientos recomendados para las API de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071189"
---
# <a name="best-practices-for-the-security-apis"></a>Procedimientos recomendados para las API de seguridad

Para ayudar a desarrollar software seguro, se recomienda usar los siguientes procedimientos recomendados al desarrollar aplicaciones. Para obtener más información, vea [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Ciclo de vida del desarrollo de seguridad

El [ciclo de vida](/previous-versions/ms995349(v=msdn.10)) de desarrollo de seguridad (SDL) es un proceso que alinea una serie de actividades y entregas centradas en la seguridad con cada fase del desarrollo de software. Estas actividades y entregas incluyen:

-   Desarrollo de modelos de amenazas
-   Uso de herramientas de análisis de código
-   Realización de revisiones de código y pruebas de seguridad

Para obtener más información sobre SDL, consulte el [blog de SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelos de amenazas

La realización de un análisis del modelo de amenazas puede ayudarle a detectar posibles puntos de ataque en el código. Para obtener más información sobre el análisis del modelo de amenazas, vea Howard, Michael y LeAle, David \[ 2003 \] , Writing Secure *Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Es posible que este recurso no esté disponible en algunos idiomas y países).

## <a name="service-packs-and-security-updates"></a>Service Packs y actualizaciones de seguridad

Los entornos de compilación y prueba deben reflejar los mismos niveles de Service Pack y actualizaciones de seguridad de la base de usuarios de destino. Se recomienda instalar los Service Pack y las actualizaciones de seguridad más recientes para cualquier plataforma o aplicación de Microsoft que forme parte del entorno de compilación y prueba, y se recomienda a los usuarios que hagan lo mismo para el entorno de aplicación finalizado. Para obtener más información sobre service packs y actualizaciones de seguridad, vea [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) y Microsoft [Security](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorización

Debe crear aplicaciones que requieran el menor privilegio posible. El uso de los privilegios mínimos posibles reduce el riesgo de que el código malintencionado coma el sistema informático. Para obtener más información sobre cómo ejecutar código en el nivel de privilegios mínimo posible, vea [Running with Special Privileges](running-with-special-privileges.md).

## <a name="more-information"></a>Más información

Para más información sobre los procedimientos recomendados, consulte los temas siguientes.



| Tema                                                                                                                        | Descripción                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ejecución con privilegios especiales](running-with-special-privileges.md)<br/>                                            | Describe las implicaciones de seguridad de los privilegios.<br/>                                                                                                                                  |
| [Evitar saturaciones de búfer](avoiding-buffer-overruns.md)<br/>                                                          | Proporciona información sobre cómo evitar saturaciones de búfer.<br/>                                                                                                                            |
| [Protección de flujo de control (CFG) ](control-flow-guard.md)<br/>                                                                | Describe las vulnerabilidades de daños en la memoria.<br/>                                                                                                                                    |
| [Creación de una DACL](creating-a-dacl.md)<br/>                                                                            | Muestra cómo crear una lista de control de acceso discrecional (DACL) mediante el lenguaje de definición de [descriptores](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de seguridad (SDDL).<br/> |
| [Control de contraseñas](handling-passwords.md)<br/>                                                                      | Describe las implicaciones de seguridad del uso de contraseñas.<br/>                                                                                                                             |
| [Cómo optimizar la búsqueda de MSDN Library](how-to-optimize-your-msdn-library-search.md)<br/>                          | Describe las opciones para buscar contenido del SDK de seguridad en MSDN Library.<br/>                                                                                                           |
| [Extensibilidad Access Control desarrolladores dinámicos](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientación básica a algunos de los puntos de extensibilidad del desarrollador para las nuevas soluciones de Access Control dinámicas.<br/>                                                                   |



 

 

