---
description: Si está escribiendo un archivo GINA para reemplazar el archivo DLL de GINA estándar de Microsoft (MSGina.dll), es posible que desee proporcionar parte o toda la funcionalidad de GINA estándar.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173461"
---
# <a name="msginadll-features"></a>MSGina.dll características

Si va a escribir un [*archivo GINA*](../secgloss/g-gly.md) para reemplazar el archivo DLL de GINA estándar de Microsoft (MSGina.dll), es posible que desee proporcionar parte o toda la funcionalidad estándar de GINA. A continuación se muestra una lista de características estándar y una breve descripción de cómo se controlan.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Los valores de clave del Registro controlan la disponibilidad o el comportamiento de muchas de estas características estándar de GINA. A menos que se indique lo contrario, estos valores de clave pertenecen a la clave del Registro Winlogon y tienen un tipo de valor \[ REG \_ SZ \] . La ruta de acceso real de [*la clave Winlogon*](../secgloss/w-gly.md) es:

**\\HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon**

-   **Notificación legal (cuadro de diálogo)**

    En algunos lugares, es legal que cualquier persona que tenga acceso a una estación de trabajo inicie sesión y comience a trabajar a menos que haya un aviso que indique que el sistema es solo para usuarios autorizados. Además, muchos usuarios quieren que los mensajes específicos de la empresa se muestren antes del inicio de sesión normal. La GINA estándar usa dos valores de clave del Registro winlogon para permitir que un sistema muestre información antes de iniciar sesión. Si alguno de los valores de clave está presente y contiene una cadena que no es NULL, se muestra un cuadro de diálogo Aviso legal antes del pantalla de inicio de sesión. Estos nombres de valor de clave se muestran en la tabla siguiente.

    

    | Nombre del valor de clave         | Contenido                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **Legalnoticecaption** | Cadena que se mostrará como título del cuadro de diálogo aviso legal |
    | **LegalNoticeText**    | Cadena que se mostrará como mensaje del cuadro de diálogo aviso legal |

    

     

-   **Mostrar apellido de usuario**

    De forma predeterminada, la pantalla de inicio de sesión muestra el nombre del último usuario en iniciar sesión correctamente en la estación de trabajo. Esta característica se controla mediante el valor de clave del Registro **DontDisplayLastUserName.** Cuando este valor de clave se establece en uno, el nombre de usuario no se muestra en el cuadro de diálogo de inicio de sesión.

-   **Inicio de sesión automático**

    Esta característica permite que un sistema inicie sesión automáticamente en un usuario cada vez que se inicia el sistema mediante la información predeterminada y deshabilita el cuadro de inicio de sesión CTRL+ALT+SUPR.

    Esta característica usa los siguientes valores de la clave Winlogon.

    

    | Value                 | Contenido                                           |
    |-----------------------|----------------------------------------------------|
    | **Autoadminlogon**    | 1                                                  |
    | **AutoLogonCount**    | Número de veces que se debe realizar un inicio de sesión automático       |
    | **DefaultUserName**   | Nombre de la cuenta de usuario                       |
    | **DefaultDomainName** | Nombre del dominio en el que se encuentra la cuenta de usuario |

    

     

    Si el valor de clave **AutoAdminLogon** está presente y contiene uno, y el valor de clave **AutoLogonCount** no está presente, se producirá un inicio de sesión automático cada vez que el usuario actual cierre la sesión o se reinicie el sistema. La cuenta en la que se inicia sesión se especifica con los valores de clave **DefaultUserName** y **DefaultDomainName.** La contraseña de la cuenta se puede especificar de una de estas dos maneras. En el caso de los equipos que ejecutan uno de los sistemas operativos Windows Server 2003 o Windows XP, la contraseña debe almacenarse como un secreto mediante la función [**LsaStorePrivateData.**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) Para obtener más información, vea [Protección de la contraseña de inicio de sesión automático.](protecting-the-automatic-logon-password.md) La otra manera de almacenar la contraseña es en texto no cifrado en la **entrada DefaultPassword** de la clave Winlogon. por motivos de seguridad, se debe evitar esta técnica. Si almacena la contraseña mediante la función **LsaStorePrivateData,** no proporcione una **entrada DefaultPassword** en la clave Winlogon.

    Si el valor de clave **AutoAdminLogon** está presente y contiene uno, y si el valor de clave **AutoLogonCount** está presente y no es cero, **AutoLogonCount** determinará el número de inicios de sesión automáticos que se producen. Cada vez que se reinicia el sistema, el valor de **AutoLogonCount** se disminuirá en uno, hasta que llegue a cero. Cuando **AutoLogonCount** alcanza el cero, no se iniciará sesión automáticamente en ninguna cuenta, el valor de clave **AutoLogonCount** y el valor de clave **DefaultPassword,** si se usan, se eliminarán del Registro y **AutoAdminLogon** se establecerá en cero.

    Hay una advertencia adicional al uso de **AutoAdminLogon:** de forma predeterminada, MSGina.dll comprueba el estado de la clave MAYÚS cuando **AutoAdminLogon** es uno. Si se mantiene la tecla MAYÚS durante el proceso de arranque, MSGina.dll omitirá el valor de la clave **AutoAdminLogon** y solicitará al usuario información de identificación y autenticación de forma interactiva. Esta es una característica útil al depurar una aplicación dedicada. Para deshabilitar el significado de la tecla MAYÚS, establezca el valor de la clave **IgnoreShiftOverride** en uno.

-   **Permitir apagado no autenticado**

    Puede configurar el [*GINA*](../secgloss/g-gly.md) predeterminado para incluir un botón **Apagar** en el cuadro de diálogo de inicio de sesión. Esto permite a los usuarios apagar el sistema sin iniciar sesión primero. El siguiente valor de clave controla si se incluye este botón.

    

    | Value                    | Descripción                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Uno para incluir el botón; cero para excluir el botón |

    

     

-   **Userinit.exe activación**

    Userinit.exe es una aplicación ejecutada por MSGina.dll cuando el usuario ha iniciado sesión. Se ejecuta en el contexto del usuario que acaba de iniciar sesión [*y*](../secgloss/c-gly.md) en el escritorio de la aplicación. Su finalidad es configurar el entorno del usuario, incluida la restauración de los usos de red, el establecimiento de la configuración del perfil, como fuentes y colores de pantalla, y la ejecución de scripts de inicio de sesión. Después de completar esas tareas, Userinit.exe ejecuta los programas de shell de usuario. Los programas de shell heredan el entorno que Userinit.exe configura. Los programas de shell específicos Userinit.exe ejecutan se almacenan en el valor de clave de **Shell** en la clave del Registro Winlogon.

    El **valor** de clave de Shell puede contener una lista separada por comas de los programas que se ejecutarán. Windows El Explorador es el programa de shell predeterminado y se ejecutará si el valor de la clave de **Shell** es NULL o no está presente. De forma predeterminada, Windows explorer aparece.

-   **Opciones de seguridad de la sesión iniciada**

    Cuando se inicia sesión, si un usuario entra en una secuencia de [*atención*](../secgloss/s-gly.md) segura (SAS), se le muestra una pantalla de opciones de seguridad. Entre las opciones enumeradas se encuentran:

    -   Apague el sistema.
    -   Cierre la sesión.
    -   Cambie la contraseña.
    -   Vaya a la lista de tareas.
    -   Bloquee la estación de trabajo.

    Una GINA de reemplazo puede proporcionar opciones similares cuando se recibe un evento sas mientras un usuario inicia sesión.

 

 
