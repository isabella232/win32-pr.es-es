---
title: Consideraciones de seguridad para las tecnologías de asistencia
description: Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- uiAccess (atributo)
- Automatización de la interfaz de usuario, atributo uiAccess
- Security, atributo uiAccess
- requestedExecutionLevel (etiqueta)
- Automatización de la interfaz de usuario, etiqueta requestedExecutionLevel
- Automatización de la interfaz de usuario, consideraciones de seguridad
- Automatización de la interfaz de usuario, archivos de manifiesto
- archivos de manifiesto
- control de cuentas de usuario
- seguridad, control de cuentas de usuario
- seguridad, archivos de manifiesto
- seguridad, etiqueta requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "105695801"
---
# <a name="security-considerations-for-assistive-technologies"></a>Consideraciones de seguridad para las tecnologías de asistencia

Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows. Las aplicaciones de tecnología de Asistencia funcionan mediante la recuperación de información del sistema operativo y de otras aplicaciones y, a continuación, la presentación de la información de forma que sea accesible para el usuario. Una aplicación de tecnología de asistencia también puede "impulsar" el sistema operativo y otras aplicaciones en función de la entrada del usuario.

La naturaleza de las aplicaciones de tecnología de asistencia requiere que crucen los límites del proceso y que tengan acceso a los procesos que se ejecutan en un nivel de integridad más alto (IL) que ellos mismos. (Las aplicaciones de tecnología de asistencia se ejecutan en IL medio). Por ejemplo, cuando el usuario intenta realizar una tarea que requiere privilegios administrativos, Windows presenta un cuadro de diálogo que pide al usuario su consentimiento para continuar. Este cuadro de diálogo se ejecuta en un IL más alto para protegerlo de la comunicación entre procesos, de modo que el software malintencionado no puede simular la entrada del usuario. De forma similar, la pantalla de inicio de sesión de escritorio se ejecuta en un IL superior para evitar que otros procesos tengan acceso a él.

Las aplicaciones de tecnología de asistencia normalmente necesitan tener acceso a los elementos de la interfaz de usuario del sistema protegidos o a otros procesos que podrían estar ejecutándose en un nivel de privilegios superior. Por lo tanto, las aplicaciones de tecnología de asistencia deben ser de confianza para el sistema y deben ejecutarse con privilegios especiales.

Para obtener acceso a los procesos de IL más altos, una aplicación de tecnología de ayuda debe establecer la marca UIAccess en el manifiesto de la aplicación e iniciarla un usuario con privilegios de administrador.

> [!NOTE]
> Los privilegios de acceso se restringen de la siguiente manera:
>
> - Una aplicación que no tiene UIAccess en el manifiesto comienza con un IL medio y no puede tener acceso a la interfaz de usuario del proceso con privilegios elevados ("medio +" IL).
> - Una aplicación que tiene UIAccess en el manifiesto y que es iniciada por un usuario que no está en el grupo de administradores, se inicia como IL "medio +" y no puede tener acceso a la interfaz de usuario con privilegios elevados (nada que se ejecute como "alto" IL, como las aplicaciones iniciadas con un **clic secundario > ejecutar como administrador**).
> - Una aplicación tiene acceso a la interfaz de usuario y es iniciada por un usuario administrador que se inicia como IL "alto" y puede tener acceso a la interfaz de usuario con privilegios elevados porque tiene el mismo IL.
>
> UIAccess no es suficiente para que un proceso se desplace por el límite de IL.

Además de tener acceso a procesos de IL más altos, una aplicación de tecnología de asistencia con estos privilegios puede ejecutarse como la aplicación de nivel superior en el orden z en cualquier momento, lo que significa que una aplicación de tecnología de asistencia puede estar visible y disponible siempre que el usuario la necesite.

> [!Important]
> Ninguno de los escenarios enumerados anteriormente proporciona acceso a la interfaz de usuario que se ejecuta en el sistema IL. Esto solo es posible si el proceso se inicia en el escritorio de control de cuentas de usuario (UAC) en sistema (y en el sistema IL). En este caso, la configuración de UIAccess no tiene ningún efecto.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Requisitos de UIAccess para aplicaciones de tecnología de asistencia

Una aplicación de tecnología de asistencia es una aplicación de escritorio Windows de Windows que interactúa con otros procesos que se ejecutan en el escritorio y en la nueva interfaz de usuario de Windows para obtener información del sistema y de las aplicaciones. A continuación, la aplicación de tecnología de asistencia puede proporcionar la información a los usuarios de accesibilidad.

Una aplicación de tecnología de asistencia obtiene acceso a otros procesos estableciendo la marca UIAccess en el manifiesto de aplicación. Para usar la marca UIAccess, una aplicación de tecnología de asistencia debe cumplir los siguientes requisitos.

-   Requiere que se muestre, interactúe o refleje información de otra aplicación para proporcionar información para un escenario de accesibilidad, o
-   Requiere la ejecución como ventana de nivel superior para obtener o mostrar esta información.

Para usar UIAccess, una aplicación de tecnología de asistencia debe:

-   Debe estar firmado con un certificado para interactuar con aplicaciones que se ejecutan en un nivel de privilegios superior.
-   Ser de confianza para el sistema. La aplicación debe instalarse en una ubicación segura que requiera un aviso de control de cuentas de usuario (UAC) para el acceso. Por ejemplo, la carpeta archivos de programa.
-   Compilar con un archivo de manifiesto que incluya la marca uiAccess.

No se debe usar UIAccess:

-   Por aplicaciones que no son tecnologías de asistencia.
-   Por aplicaciones de tecnología de asistencia que muestran información o interfaz de usuario que no es relevante para el escenario de accesibilidad de destino.
-   Por aplicaciones que solo quieren aparecer por encima de otras aplicaciones en la nueva interfaz de usuario de Windows.
    > [!Note]  
    > Las aplicaciones desarrolladas para la nueva interfaz de usuario de Windows no tienen UIAccess como una opción disponible.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Establecer UIAccess en el archivo de manifiesto de aplicación

Para obtener acceso a la interfaz de usuario del sistema protegida, las aplicaciones deben compilarse con un archivo de manifiesto que incluya un atributo especial en el archivo de manifiesto. Este atributo **UIAccess** se incluye en la etiqueta **requestedExecutionLevel** , tal como se muestra en el ejemplo de código siguiente.


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



El valor del atributo **LEVEL** en este código es solo un ejemplo.

**UIAccess** es "false" de forma predeterminada. Si se omite el atributo o si no hay ningún manifiesto, la aplicación no puede obtener acceso a la interfaz de usuario protegida.

Para obtener más información sobre la seguridad de Windows, sobre la firma de aplicaciones y sobre la creación de manifiestos, consulte [el artículo sobre el desarrollador de Windows Vista y Windows Server 2008: requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10)) en MSDN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 