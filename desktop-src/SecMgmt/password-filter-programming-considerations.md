---
description: Explica las consideraciones para la implementación de funciones de exportación de filtros de contraseñas.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Consideraciones sobre la programación de filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666399"
---
# <a name="password-filter-programming-considerations"></a>Consideraciones sobre la programación de filtros de contraseña

Al implementar funciones de exportación de [*filtros de contraseña*](/windows/desktop/SecGloss/p-gly) , tenga en cuenta las consideraciones siguientes:

-   Tenga mucho cuidado al trabajar con contraseñas de [*texto sin formato*](/windows/desktop/SecGloss/p-gly) . El envío de contraseñas sin formato a través de redes podría poner en peligro la seguridad. Los "rastreadores" de red pueden ver fácilmente el tráfico de contraseñas sin formato.
-   Borre toda la memoria usada para almacenar las contraseñas mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memoria.
-   Todos los búferes pasados a las rutinas de filtro y notificación de contraseña deben tratarse como de solo lectura. La escritura de datos en estos búferes puede provocar un comportamiento inestable.
-   Todas las rutinas de filtrado y notificación de contraseña deben ser seguras para subprocesos. Use secciones críticas u otras técnicas de programación sincrónicas para proteger los datos cuando corresponda.
-   La notificación y el filtrado de contraseñas tienen lugar solo en el equipo que aloja la cuenta.
-   Todos los controladores de dominio son grabables, por lo que los paquetes de filtros de contraseña deben estar presentes en todos los controladores de dominio.

    **Dominios de Windows NT 4,0:** La notificación en las cuentas de dominio solo tiene lugar en el controlador de dominio principal. Además del controlador de dominio principal, los paquetes de filtro de contraseña deben instalarse en todos los controladores de dominio de copia de seguridad para permitir que las notificaciones continúen en caso de que se realicen cambios en el rol de servidor.

-   Todos los archivos dll de filtro de contraseña se ejecutan en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de la cuenta de sistema local.



| Para información acerca de                                                                                                                     | Vea                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cómo instalar y registrar su propia DLL de [*filtro de contraseñas*](/windows/desktop/SecGloss/p-gly) . | [Instalación y registro de un archivo DLL de filtro de contraseñas](installing-and-registering-a-password-filter-dll.md) |
| El archivo DLL de filtro de contraseña proporcionado por Microsoft.                                                                                            | [Aplicación segura de contraseñas y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Exportar funciones implementadas por un archivo DLL de filtro de contraseñas.                                                                                    | [Funciones de filtro de contraseñas](management-functions.md)                          |



 

 

 
