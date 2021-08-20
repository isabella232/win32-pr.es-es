---
description: Corrección de ActiveX de compatibilidad de instalación de aplicaciones para usuarios estándar
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Corrección de ActiveX de compatibilidad de instalación de aplicaciones para usuarios estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31dbcf8dfddd7e35a8a446f4b73dd1e5324cbe4695590511fa1cb220700b2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994775"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Corrección de ActiveX de compatibilidad de instalación de aplicaciones para usuarios estándar

Para desarrollar un entorno de escritorio seguro, debe mitigar las amenazas de los controles ActiveX malintencionados y proporcionar un nivel adecuado de compatibilidad de aplicaciones en su entorno. Un *control ActiveX* es un fragmento de código ejecutable (normalmente un archivo OCX que se empaqueta dentro de un archivo de archivador) que se instala y se ejecuta a través de Windows Internet Explorer. Puede crear controles ActiveX para agregar funcionalidad a las aplicaciones web que no se puede lograr fácilmente mediante código HTML estándar o un script simple.

La instalación de controles ActiveX se convierte en un problema de compatibilidad cuando la migración a Windows 7 incluye una transición a usuarios estándar. Este tipo de transición es un procedimiento recomendado común en el que los profesionales de TI mueven su entorno a una [cuenta de usuario estándar.](https://support.microsoft.com/hub/4338813/windows-help) Esta transición no es un requisito para implementar Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX Instalación de controles

ActiveX controles tienen un modelo de implementación de descarga y ejecución simple. ActiveX se instalan y se ejecutan a través del elemento **de objeto** HTML. El **atributo CODEBASE** de este elemento indica a Internet Explorer (mediante una dirección URL) dónde obtener el control si aún no está instalado en el equipo del usuario. En ese caso, Internet Explorer descarga el paquete de instalación asociado, realiza la comprobación de confianza en el objeto y solicita al usuario permiso de instalación en Internet Explorer.

Durante la instalación, la página de representación registra y ejecuta el control . Una vez instalado el control, cualquier usuario estándar puede ejecutar el control. Este sencillo mecanismo de distribución y ejecución proporciona una manera sencilla de distribuir los componentes a los usuarios de la aplicación web. Sin embargo, los usuarios de la cuenta estándar no pueden instalar directamente los controles de ActiveX equipo y es posible que necesiten privilegios de administrador para completar la instalación.

## <a name="activex-installer-service-axis"></a>ActiveX Servicio de instalador (AXIS)

El ActiveX instalador de aplicaciones (AXIS) permite implementar controles ActiveX mediante directiva de grupo en equipos de una organización. Puede configurar AXIS directiva de grupo configuración, que puede modificar mediante el Consola de administración de directivas de grupo (GPMC) o el Editor de directivas de grupo local.

Hay dos configuraciones de directiva para AXIS:

-   La configuración de directiva Sitios de instalación aprobados para ActiveX Controls consta de una lista de sitios de instalación aprobados, que el EJE usa para determinar si se puede instalar un control ActiveX de instalación.
-   La ActiveX de instalación de sitios en la configuración de directiva zonas de confianza identifica cómo se pueden usar las zonas de sitios de confianza para instalar ActiveX controles.

Cuando un sitio web intenta instalar un control ActiveX, axis comprueba si la dirección URL del sitio web aparece en la lista de sitios de instalación aprobados o como parte de la zona de sitios de confianza. Si el sitio está en cualquiera de estas listas, AXIS se asegura de que el sitio cumple los requisitos que define la directiva. Si el sitio y el control ActiveX cumplen todos los requisitos de la configuración de directiva, se instala el control. Para obtener más información, vea la página relativa a la [administración del Servicio de instalador de ActiveX](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
