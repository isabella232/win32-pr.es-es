---
description: El Windows de filtro de contraseñas, Passfilt.dll, se ejecuta en el contexto de seguridad de la cuenta del sistema local y le ayuda a filtrar las contraseñas de dominio o de cuenta local.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalación y registro de un archivo DLL de filtro de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374875"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Instalación y registro de un archivo DLL de filtro de contraseña

Puede usar el filtro de Windows contraseña para filtrar las contraseñas de dominio o de cuenta local. Para usar el filtro de contraseña para las cuentas de dominio, instale y registre el archivo DLL en cada controlador de dominio del dominio.

Realice los pasos siguientes para instalar el filtro de contraseña. Puede realizar estos pasos manualmente o escribir un instalador para realizar estos pasos. Debe ser administrador o pertenecer al grupo de administradores para realizar estos pasos.

**Para instalar y registrar un archivo DLL Windows de filtro de contraseña**

1.  Copie el archivo DLL en el Windows de instalación en el controlador de dominio o en el equipo local. En las instalaciones estándar, la carpeta predeterminada \\ es Windows \\ System32. Asegúrese de crear un archivo DLL de filtro de contraseña de 32 bits para equipos de 32 bits y un archivo DLL de filtro de contraseña de 64 bits para equipos de 64 bits y, a continuación, cópielos en la ubicación adecuada.
2.  Para registrar el filtro de contraseña, actualice la siguiente clave del Registro del sistema:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Si existe **el valor Paquetes** de *notificación REG_MULTI_SZ* tipo , agregue el nombre del archivo DLL a los datos de valor existentes. No sobrescriba los valores existentes y no incluya la .dll existente.

    Si el **valor Paquetes** de notificación no existe, cándalo, asíézcale el tipo REG_MULTI_SZ y, *a* continuación, especifique el nombre del archivo DLL para los datos de valor. No incluya la .dll extensión.

    El **valor Paquetes de** notificación puede agregar varios paquetes.

3.  Busque la configuración de complejidad de la contraseña.

    En Panel de control, haga clic en Rendimiento y mantenimiento **,** herramientas administrativas **,** haga doble clic en Directiva de seguridad **local,** haga doble clic en Directivas de cuentay, a continuación, haga doble clic en Directiva de **contraseñas.**

4.  Para aplicar el filtro predeterminado Windows contraseña y el filtro de contraseña personalizado, asegúrese de que la configuración de directiva Contraseñas debe cumplir **los** requisitos de complejidad está habilitada. De lo contrario, deshabilite **la configuración de directiva Contraseñas debe cumplir los requisitos** de complejidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones sobre la programación de filtros de contraseñas](password-filter-programming-considerations.md)
</dt> <dt>

[Aplicación de contraseñas seguras y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Funciones de filtro de contraseña](management-functions.md)
</dt> </dl>

 

 



