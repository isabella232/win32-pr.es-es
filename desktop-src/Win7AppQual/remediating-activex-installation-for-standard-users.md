---
description: .
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Corregir problemas de compatibilidad de la instalación de ActiveX para usuarios estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e50ed2aa9e428164e39b377b65c418d82df1e5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820271"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Corregir problemas de compatibilidad de la instalación de ActiveX para usuarios estándar

Para desarrollar un entorno de escritorio seguro, debe mitigar las amenazas de los controles ActiveX malintencionados y proporcionar un nivel adecuado de compatibilidad de aplicaciones en su entorno. Un *control ActiveX* es un fragmento de código ejecutable (normalmente un archivo ocx empaquetado dentro de un archivo. cab) que se instala y ejecuta a través de Windows Internet Explorer. Puede crear controles ActiveX para agregar funcionalidad a las aplicaciones web que no se pueden lograr fácilmente mediante código HTML estándar o un script sencillo.

La instalación de controles ActiveX se convierte en un problema de compatibilidad cuando la migración a Windows 7 incluye una transición a usuarios estándar. Este tipo de transición es una práctica recomendada común en la que los profesionales de ti mueven su entorno a una [cuenta de usuario estándar](https://support.microsoft.com/hub/4338813/windows-help). Esta transición no es un requisito para la implementación de Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>Instalación de controles ActiveX

Los controles ActiveX tienen un modelo de implementación de descarga y ejecución sencillo. Los controles ActiveX se instalan y se ejecutan a través del elemento de **objeto** HTML. El atributo **codebase** de este elemento indica a Internet Explorer (mediante una dirección URL) dónde obtener el control si aún no está instalado en el equipo del usuario. En ese caso, Internet Explorer descarga el paquete de instalación asociado, realiza la comprobación de confianza en el objeto y solicita al usuario permiso de instalación en Internet Explorer.

Durante la instalación, la página de representación se registra y ejecuta el control. Una vez instalado el control, los usuarios estándar pueden ejecutar el control. Este sencillo mecanismo de distribución y ejecución proporciona una manera sencilla de distribuir los componentes a los usuarios de la aplicación Web. Sin embargo, los usuarios de cuentas estándar no pueden instalar directamente controles ActiveX por equipo y es posible que necesiten privilegios de administrador para completar la instalación.

## <a name="activex-installer-service-axis"></a>Servicio de instalador de ActiveX (eje)

El servicio de instalador de ActiveX (eje) permite implementar controles ActiveX mediante directiva de grupo en los equipos de una organización. Puede configurar AXIS by directiva de grupo valores, que puede modificar mediante el Consola de administración de directivas de grupo (GPMC) o el Editor de directivas de grupo local.

Hay dos configuraciones de directiva para AXIS:

-   La configuración de directiva sitios de instalación aprobados para controles ActiveX consta de una lista de sitios de instalación aprobados, que el eje usa para determinar si se puede instalar un control ActiveX.
-   La configuración de directiva Directiva de instalación de ActiveX para sitios en zonas de confianza identifica cómo se pueden usar las zonas de sitios de confianza para instalar controles ActiveX.

Cuando un sitio web intenta instalar un control ActiveX, el eje comprueba para ver si la dirección URL del sitio web aparece en la lista de sitios de instalación aprobados o como parte de la zona de sitios de confianza. Si el sitio se encuentra en cualquiera de estas listas, el eje se asegura de que el sitio cumple los requisitos que define la Directiva. Si el sitio y el control ActiveX cumplen todos los requisitos de la configuración de directiva, se instala el control. Para obtener más información, vea la página relativa a la [administración del Servicio de instalador de ActiveX](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
