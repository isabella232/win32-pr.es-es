---
description: Explica las consideraciones para la implementación de las funciones de exportación de filtro de contraseña.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Consideraciones sobre la programación del filtro de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9270a08c51b4b3e6b07923ad9461dc2e2dd418c3be1f1a181c07f940d71ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005093"
---
# <a name="password-filter-programming-considerations"></a>Consideraciones sobre la programación del filtro de contraseñas

Al implementar funciones [*de exportación de filtro*](/windows/desktop/SecGloss/p-gly) de contraseña, tenga en cuenta las siguientes consideraciones:

-   Al trabajar con contraseñas [*de texto no cifrado,*](/windows/desktop/SecGloss/p-gly) debe tener mucho cuidado. El envío de contraseñas de texto no cifrado a través de redes podría poner en peligro la seguridad. Los "sniffers" de red pueden observar fácilmente el tráfico de contraseñas de texto no cifrado.
-   Borre toda la memoria usada para almacenar contraseñas mediante una llamada a la [**función SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memoria.
-   Todos los búferes pasados a las rutinas de filtro y notificación de contraseña deben tratarse como de solo lectura. La escritura de datos en estos búferes puede provocar un comportamiento inestable.
-   Todas las rutinas de filtro y notificación de contraseñas deben ser seguras para subprocesos. Use secciones críticas u otras técnicas de programación sincrónicas para proteger los datos cuando corresponda.
-   La notificación y el filtrado de contraseñas solo se llevan a cabo en el equipo que aloja la cuenta.
-   Todos los controladores de dominio se pueden escribir, por lo que los paquetes de filtro de contraseña deben estar presentes en todos los controladores de dominio.

    **Windows dominios NT 4.0:** La notificación en las cuentas de dominio tiene lugar solo en el controlador de dominio principal. Además del controlador de dominio principal, los paquetes de filtro de contraseñas deben instalarse en todos los controladores de dominio de copia de seguridad para permitir que las notificaciones continúen en caso de que se cambie el rol de servidor.

-   Todos los archivos DLL de filtro de contraseña se ejecutan en [*el contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de la cuenta del sistema local.



| Para información acerca de                                                                                                                     | Vea                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cómo instalar y registrar su propio archivo DLL [*de filtro de*](/windows/desktop/SecGloss/p-gly) contraseña. | [Instalar y registrar un archivo DLL de filtro de contraseña](installing-and-registering-a-password-filter-dll.md) |
| Dll de filtro de contraseña proporcionada por Microsoft.                                                                                            | [Aplicación de contraseñas seguras y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Exportar funciones implementadas por un archivo DLL de filtro de contraseña.                                                                                    | [Funciones de filtro de contraseña](management-functions.md)                          |



 

 

 
