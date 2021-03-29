---
description: Si está escribiendo una GINA para reemplazar el archivo DLL de GINA estándar de Microsoft (MSGina.dll), es posible que desee proporcionar alguna o todas las funciones de GINA estándar.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911873"
---
# <a name="msginadll-features"></a>MSGina.dll características

Si está escribiendo una [*Gina*](../secgloss/g-gly.md) para reemplazar el archivo dll de Gina estándar de Microsoft (MSGina.dll), es posible que desee proporcionar alguna o todas las funciones de Gina estándar. A continuación se muestra una lista de las características estándar y una breve descripción de cómo se controlan.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Los valores de clave del registro controlan la disponibilidad o el comportamiento de muchas de estas características estándar de GINA. A menos que se indique lo contrario, estos valores de clave pertenecen a la clave del registro Winlogon y tienen un tipo de valor de \[ reg \_ SZ \] . La ruta de acceso real de la clave [*Winlogon*](../secgloss/w-gly.md) es la siguiente:

**\\HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **Cuadro de diálogo notificación legal**

    En algunos lugares, es válido para cualquier persona que tenga acceso a una estación de trabajo iniciar sesión y empezar a trabajar a menos que haya un aviso que indique que el sistema es solo para usuarios autorizados. Además, muchos usuarios quieren que se muestren mensajes específicos de la empresa antes del inicio de sesión normal. GINA estándar usa dos valores de clave del registro de Winlogon para permitir que un sistema muestre información antes del inicio de sesión. Si cualquiera de los dos valores de clave está presente y contiene una cadena que no es null, se muestra un cuadro de diálogo de aviso legal antes de la pantalla de bienvenida habitual. Estos nombres de valor de clave se muestran en la tabla siguiente.

    

    | Nombre del valor de clave         | Contenido                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Cadena que se va a mostrar como título del cuadro de diálogo aviso legal. |
    | **LegalNoticeText**    | Cadena que se va a mostrar como mensaje del cuadro de diálogo aviso legal. |

    

     

-   **Mostrar el último nombre de usuario**

    De forma predeterminada, la pantalla de inicio de sesión muestra el nombre del último usuario para iniciar sesión correctamente en la estación de trabajo. Esta característica se controla mediante el valor de la clave del registro **DontDisplayLastUserName** . Cuando este valor de clave se establece en uno, el nombre de usuario no se muestra en el cuadro de diálogo de inicio de sesión.

-   **Inicio de sesión automático**

    Esta característica permite que un sistema inicie sesión automáticamente a un usuario cada vez que se inicia el sistema mediante la información predeterminada y se deshabilita el cuadro de inicio de sesión CTRL + ALT + SUPR.

    Esta característica usa los siguientes valores de la clave Winlogon.

    

    | Value                 | Contenido                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | El número de veces que se realiza un inicio de sesión automático       |
    | **DefaultUserName**   | El nombre de la cuenta de usuario                       |
    | **DefaultDomainName** | Nombre del dominio en el que se encuentra la cuenta de usuario |

    

     

    Si el valor de clave **AutoAdminLogon** está presente y contiene uno, y el valor de clave **AutoLogonCount** no está presente, se producirá un inicio de sesión automático cada vez que el usuario actual cierre la sesión o se reinicie el sistema. La cuenta en la que se inicia sesión se especifica mediante los valores de clave **DefaultUserName** y **DefaultDomainName** . La contraseña de la cuenta se puede especificar de una de las dos maneras siguientes. En el caso de los equipos que ejecutan uno de los sistemas operativos Windows Server 2003 o Windows XP, la contraseña debe almacenarse como un secreto mediante la función [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Para obtener más información, consulte [protección de la contraseña de inicio de sesión automático](protecting-the-automatic-logon-password.md). La otra forma de almacenar la contraseña es en texto no cifrado en la entrada **DefaultPassword** de la clave Winlogon; por motivos de seguridad, esta técnica debe evitarse. Si almacena la contraseña mediante la función **LsaStorePrivateData** , no proporcione una entrada **DefaultPassword** en la clave Winlogon.

    Si el valor de clave **AutoAdminLogon** está presente y contiene uno, y si el valor de clave **AutoLogonCount** está presente y no es cero, **AutoLogonCount** determinará el número de inicios de sesión automáticos que se producen. Cada vez que se reinicia el sistema, el valor de **AutoLogonCount** disminuirá en uno, hasta que llegue a cero. Cuando **AutoLogonCount** llega a cero, no se iniciará sesión automáticamente en ninguna cuenta, el valor de clave **AutoLogonCount** y el valor de clave **DefaultPassword** , si se usan, se eliminarán del registro y **AutoAdminLogon** se establecerá en cero.

    Hay una advertencia adicional sobre el uso de **AutoAdminLogon**: de forma predeterminada, MSGina.dll comprueba el estado de la tecla Mayús cuando **AutoAdminLogon** es uno. Si se mantiene presionada la tecla Mayús durante el proceso de arranque, MSGina.dll omitirá el valor de clave **AutoAdminLogon** y solicitará al usuario información de identificación y autenticación interactivamente. Se trata de una característica útil al depurar una aplicación dedicada. Para deshabilitar el significado de la tecla Mayús, establezca el valor de la clave **IgnoreShiftOverride** en uno.

-   **Permitir apagado no autenticado**

    Puede configurar [*Gina*](../secgloss/g-gly.md) predeterminada para incluir un botón de **apagado** en el cuadro de diálogo de inicio de sesión. Esto permite a los usuarios apagar el sistema sin iniciar sesión por primera vez. El siguiente valor de clave controla si este botón está incluido.

    

    | Value                    | Descripción                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Uno para incluir el botón; cero para excluir el botón |

    

     

-   **Activación deUserinit.exe**

    Userinit.exe es una aplicación que ejecuta MSGina.dll cuando el usuario ha iniciado sesión. Se ejecuta en el [*contexto*](../secgloss/c-gly.md) del usuario que acaba de iniciar sesión y en el escritorio de la aplicación. Su finalidad es configurar el entorno del usuario, incluida la restauración de los usos de la red, el establecimiento de la configuración del perfil, como fuentes y colores de la pantalla, y la ejecución de scripts de inicio de sesión. Después de completar estas tareas, Userinit.exe ejecuta los programas de Shell de usuario. Los programas de Shell heredan el entorno que Userinit.exe configura. Los programas de Shell específicos que se ejecutan Userinit.exe se almacenan en el valor de la clave de **Shell** en la clave del registro Winlogon.

    El valor de la clave de **Shell** puede contener una lista separada por comas de los programas que se van a ejecutar. El explorador de Windows es el programa de shell predeterminado y se ejecutará si el valor de la clave de **Shell** es null o no está presente. De forma predeterminada, se muestra el explorador de Windows.

-   **Opciones de seguridad de la sesión iniciada**

    Cuando se inicia sesión, si un usuario escribe una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS), se muestra una pantalla de opciones de seguridad en el usuario. Entre las opciones que se muestran se encuentran:

    -   Apague el sistema.
    -   Cierre la sesión.
    -   Cambie la contraseña.
    -   Vaya a la lista de tareas.
    -   Bloquee la estación de trabajo.

    Una GINA de reemplazo puede proporcionar opciones similares cuando se recibe un evento de SAS mientras un usuario inicia sesión.

 

 
