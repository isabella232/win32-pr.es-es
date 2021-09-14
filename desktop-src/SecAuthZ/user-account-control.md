---
description: Permite a los usuarios realizar tareas comunes como no administradores, denominados usuarios estándar y como administradores sin tener que cambiar de usuario, cerrar sesión o usar Ejecutar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Control de cuentas de usuario (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253646"
---
# <a name="user-account-control-authorization"></a>Control de cuentas de usuario (autorización)

El control de cuentas de usuario (UAC) permite a los usuarios realizar tareas comunes como no administradores, denominados usuarios estándar y como administradores sin tener que cambiar de usuario, cerrar sesión o usar Ejecutar **como**. El comportamiento de UAC para la configuración "No notificar nunca" ya no deshabilita UAC. La configuración "No notificar nunca" proporciona un token dividido y siempre eleva automáticamente los privilegios necesarios. Esta sutildad puede hacer que la aplicación tenga problemas de compatibilidad. Todavía puede deshabilitar UAC mediante directivas de grupo o estableciendo manualmente la clave del Registro.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** La opción "No notificar nunca" deshabilita UAC.

Por ejemplo, si realiza los pasos siguientes para cambiar la configuración "No notificar nunca", obtiene resultados diferentes al intentar crear un archivo en una carpeta que requiere privilegios elevados. El Windows 8 comportamiento es denegar el acceso. El Windows 7 le permite crear el File.txt archivo.

1.  Pulse o haga clic **en Iniciar.** En el cuadro de búsqueda, escriba "Cambiar la configuración del control de cuentas de usuario".
2.  Pulse o haga clic **en Cambiar configuración de Control de cuentas de** usuario para abrirlo.
3.  Mueva el control deslizante a **No notificar nunca a**.
4.  Pulse o haga clic **en Aceptar.**
5.  Reinicie el equipo.
6.  Pulse o haga clic **en Inicio** y, a continuación, **en Ejecutar.** En el **cuadro** Abrir, escriba "Cmd.exe". Tenga en cuenta que el título de la ventana no contiene la cadena "Administrador".
7.  Escriba "echo > %windir% \\ system32 \\File.txt".

UAC se agregó en Windows Server 2008 y Windows Vista. Una cuenta de usuario estándar es sinónimo de una cuenta de usuario Windows XP. Las cuentas de usuario que son miembros del grupo local Administradores ejecutarán la mayoría de las aplicaciones como un usuario estándar.

Para obtener información sobre UAC, consulte los temas siguientes.



| Tema                                                                                                                                        | Descripción                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Directrices para el control de cuentas de usuario en el desarrollo de la interfaz de usuario](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Información general sobre UAC.<br/>                                                                                                     |
| [Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelos para desarrollar aplicaciones que realizan operaciones que requieren privilegios administrativos, pero que se ejecutan como un usuario estándar.<br/> |
| [Referencia de autorización](authorization-reference.md)<br/>                                                                            | Información detallada sobre las funciones de autorización, interfaces, estructuras y otros elementos de programación.<br/>                        |



 

 

 




