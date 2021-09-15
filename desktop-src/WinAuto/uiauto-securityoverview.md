---
title: Consideraciones de seguridad para las tecnologías de asistencia
description: Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- Atributo uiAccess
- Automatización de la interfaz de usuario,atributo uiAccess
- security,uiAccess attribute
- requestedExecutionLevel, etiqueta
- Automatización de la interfaz de usuario,requestedExecutionLevel etiqueta
- Automatización de la interfaz de usuario, consideraciones de seguridad
- Automatización de la interfaz de usuario,archivos de manifiesto
- archivos de manifiesto
- control de cuentas de usuario
- seguridad, control de cuentas de usuario
- security,manifest files
- security,requestedExecutionLevel tag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359242"
---
# <a name="security-considerations-for-assistive-technologies"></a>Consideraciones de seguridad para las tecnologías de asistencia

Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows. Las aplicaciones de tecnología de asistencia funcionan mediante la recuperación de información del sistema operativo y otras aplicaciones y, a continuación, la presentación de la información de una manera accesible para el usuario. Una aplicación de tecnología de asistencia también puede "controlar" mediante programación el sistema operativo y otras aplicaciones en función de la entrada del usuario.

La naturaleza de las aplicaciones de tecnología de asistencia requiere que crucen los límites del proceso y que tengan acceso a los procesos que se ejecutan en un nivel de integridad (IL) más alto que ellos mismos. (Una aplicación de tecnología de asistencia se ejecuta en il medio). Por ejemplo, cuando el usuario intenta realizar una tarea que requiere privilegios administrativos, Windows un cuadro de diálogo en el que se solicita al usuario su consentimiento para continuar. Este cuadro de diálogo se ejecuta en un IL superior para protegerlo de la comunicación entre procesos, de modo que el software malintencionado no pueda simular la entrada del usuario. De forma similar, la pantalla de inicio de sesión de escritorio se ejecuta en un IL superior para evitar que otros procesos accedan a ella.

Las aplicaciones de tecnología de asistencia normalmente necesitan acceso a los elementos protegidos de la interfaz de usuario del sistema o a otros procesos que podrían ejecutarse en un nivel de privilegios superior. Por lo tanto, las aplicaciones de tecnología de asistencia deben ser de confianza para el sistema y deben ejecutarse con privilegios especiales.

Para obtener acceso a procesos de IL superiores, una aplicación de tecnología de asistencia debe establecer la marca UIAccess en el manifiesto de la aplicación y ser iniciada por un usuario con privilegios de administrador.

> [!NOTE]
> Los privilegios de acceso están restringidos de la manera siguiente:
>
> - Una aplicación que no tiene UIAccess en el manifiesto comienza con il medio y no puede acceder a la interfaz de usuario de proceso con privilegios elevados ("IL medio+").
> - Una aplicación que tiene UIAccess en el manifiesto y la inicia un usuario que no está en el grupo de administradores, se inicia como IL "medio+" y no puede acceder a la interfaz de usuario con privilegios elevados (nada que se ejecute como IL "alto", como las aplicaciones iniciadas a través de un clic con el botón derecho **-> Ejecutar como administrador).**
> - Una aplicación tiene acceso a la interfaz de usuario y un usuario administrador inicia como IL "alto" y puede acceder a la interfaz de usuario con privilegios elevados porque tiene el mismo IL.
>
> UIAccess no es suficiente para que un proceso suba a través del límite de IL.

Además de tener acceso a procesos de IL superiores, una aplicación de tecnología de asistencia con estos privilegios se puede ejecutar como la aplicación más importante en el orden z en cualquier momento, lo que significa que una aplicación de tecnología de asistencia puede estar visible y disponible cada vez que el usuario la necesite.

> [!Important]
> Ninguno de los escenarios enumerados anteriormente proporciona acceso a la interfaz de usuario que se ejecuta en el IL del sistema. Esto solo es posible si el proceso se inicia en el escritorio de control de cuentas de usuario (UAC) en SYSTEM (e IL del sistema). En este caso, establecer UIAccess no tiene ningún efecto.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Requisitos de UIAccess para aplicaciones de tecnología de asistencia

Una aplicación de tecnología de asistencia es una aplicación de escritorio Windows Windows que interactúa con otros procesos que se ejecutan en el escritorio y en la nueva interfaz de usuario de Windows para obtener información del sistema y las aplicaciones. La aplicación de tecnología de asistencia puede proporcionar la información a los usuarios de accesibilidad.

Una aplicación de tecnología de asistencia obtiene acceso a otros procesos estableciendo la marca UIAccess en el manifiesto de aplicación. Para usar la marca UIAccess, una aplicación de tecnología de asistencia debe cumplir los siguientes requisitos.

-   Requerir mostrar, interactuar o reflejar información de otra aplicación para proporcionar información para un escenario de accesibilidad o
-   Requerir que se ejecute como la ventana de nivel superior para obtener o mostrar esta información.

Para usar UIAccess, una aplicación de tecnología de asistencia debe:

-   Estar firmado con un certificado para interactuar con aplicaciones que se ejecutan en un nivel de privilegios superior.
-   Ser de confianza para el sistema. La aplicación debe instalarse en una ubicación segura que requiera un símbolo del sistema de control de cuentas de usuario (UAC) para el acceso. Por ejemplo, la carpeta Archivos de programa.
-   Se debe construir con un archivo de manifiesto que incluya la marca uiAccess.

UIAccess no debe usarse:

-   Por aplicaciones que no son tecnologías de asistencia.
-   Mediante aplicaciones de tecnología de asistencia que muestran información o interfaz de usuario que no es relevante para el escenario de accesibilidad al que se dirigirán.
-   Por aplicaciones que solo quieren aparecer encima de otras aplicaciones en la nueva interfaz Windows usuario.
    > [!Note]  
    > Las aplicaciones desarrolladas para la nueva Windows interfaz de usuario no tienen UIAccess como opción disponible.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Configuración de UIAccess en el archivo de manifiesto de aplicación

Para obtener acceso a la interfaz de usuario del sistema protegido, las aplicaciones deben crearse con un archivo de manifiesto que incluya un atributo especial en el archivo de manifiesto. Este **atributo uiAccess** se incluye en la **etiqueta requestedExecutionLevel,** como se muestra en el ejemplo de código siguiente.


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



El valor del atributo **level** de este código es solo un ejemplo.

**UIAccess** es "false" de forma predeterminada. Si se omite el atributo o si no hay ningún manifiesto, la aplicación no puede obtener acceso a la interfaz de usuario protegida.

Para obtener más información sobre la seguridad de Windows, sobre la firma de aplicaciones y la creación de manifiestos, vea [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) en MSDN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 