---
description: El archivo DLL de filtro de contraseñas de Windows, Passfilt.dll, se ejecuta en el contexto de seguridad de la cuenta de sistema local y ayuda a filtrar contraseñas de cuentas locales o de dominio.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalación y registro de un archivo DLL de filtro de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910062"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Instalación y registro de un archivo DLL de filtro de contraseñas

Puede usar el filtro de contraseñas de Windows para filtrar contraseñas de cuentas locales o de dominio. Para usar el filtro de contraseñas para las cuentas de dominio, instale y registre el archivo DLL en cada controlador de dominio del dominio.

Realice los pasos siguientes para instalar el filtro de contraseña. Puede realizar estos pasos manualmente o puede escribir un instalador para realizar estos pasos. Debe ser administrador o pertenecer al grupo de administradores para realizar estos pasos.

**Para instalar y registrar un archivo DLL de filtro de contraseñas de Windows**

1.  Copie el archivo DLL en el directorio de instalación de Windows en el controlador de dominio o en el equipo local. En las instalaciones estándar, la carpeta predeterminada es \\ Windows \\ system32. Asegúrese de crear un archivo DLL de filtro de contraseña de 32 bits para equipos de 32 bits y un archivo DLL de filtro de contraseñas de 64 bits para equipos de 64 bits y, a continuación, cópielos en la ubicación adecuada.
2.  Para registrar el filtro de contraseña, actualice la siguiente clave del registro del sistema:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Si existe la subclave de **paquetes de notificación** , agregue el nombre de la dll a los datos de valor existentes. No sobrescriba los valores existentes y no incluya la extensión. dll.

    Si la subclave de los **paquetes de notificación** no existe, agréguela y especifique el nombre del archivo DLL para los datos del valor. No incluya la extensión. dll.

    La subclave de **paquetes de notificación** puede agregar varios paquetes.

3.  Busque la configuración de complejidad de la contraseña.

    En el panel de control, haga clic en **rendimiento y mantenimiento**, haga clic en **herramientas administrativas**, haga doble clic en **Directiva de seguridad local**, haga doble clic en **directivas de cuenta** y, a continuación, haga doble clic en **Directiva de contraseñas**.

4.  Para aplicar el filtro de contraseña de Windows predeterminado y el filtro de contraseña personalizado, asegúrese de que la configuración de la Directiva las **contraseñas deben cumplir los requisitos de complejidad** está habilitada. De lo contrario, deshabilite la configuración de directiva las **contraseñas deben cumplir los requisitos de complejidad** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones sobre la programación de filtros de contraseña](password-filter-programming-considerations.md)
</dt> <dt>

[Aplicación segura de contraseñas y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Funciones de filtro de contraseñas](management-functions.md)
</dt> </dl>

 

 



