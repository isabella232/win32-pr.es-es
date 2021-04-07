---
description: Permite a los usuarios realizar tareas comunes como no administradores, denominadas usuarios estándar y como administradores sin necesidad de cambiar de usuario, cerrar la sesión o usar ejecutar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Control de cuentas de usuario (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002684"
---
# <a name="user-account-control-authorization"></a>Control de cuentas de usuario (autorización)

Control de cuentas de usuario (UAC) permite a los usuarios realizar tareas comunes como no administradores, denominadas usuarios estándar y como administradores sin necesidad de cambiar de usuario, cerrar la sesión o usar **Ejecutar como**. El comportamiento de UAC para el valor "no notificar nunca" ya no deshabilita UAC. La configuración "no notificar nunca" proporciona un token de división y siempre eleva automáticamente el privilegio requerido. Esta sutileza puede hacer que la aplicación tenga problemas de compatibilidad. Todavía puede deshabilitar UAC mediante el uso de directivas de grupo o la configuración manual de la clave del registro.

**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** La configuración "no notificar nunca" deshabilita UAC.

Por ejemplo, si realiza los siguientes pasos para cambiar la configuración de "no notificar nunca", obtendrá resultados diferentes cuando intente crear un archivo en una carpeta que requiera privilegios elevados. El comportamiento de Windows 8 es denegar el acceso. El comportamiento de Windows 7 le permite crear el archivo de File.txt.

1.  Pulse o haga clic en **iniciar**. En el cuadro de búsqueda, escriba "cambiar la configuración del control de cuentas de usuario".
2.  Pulse o haga clic en **cambiar la configuración del control de cuentas de usuario** para abrirla.
3.  Mueva el control deslizante a no **notificar nunca**.
4.  Pulse o haga clic en **Aceptar**.
5.  Reinicie el equipo.
6.  Pulse o haga clic en **iniciar** y, a continuación, en **Ejecutar**. En el cuadro **abrir** , escriba "Cmd.exe". Tenga en cuenta que el título de la ventana no contiene la cadena "administrador".
7.  Escriba "echo >% WINDIR% \\ system32 \\File.txt".

UAC se agregó en Windows Server 2008 y Windows Vista. Una cuenta de usuario estándar es sinónimo de una cuenta de usuario en Windows XP. Las cuentas de usuario que son miembros del grupo local Administradores ejecutarán la mayoría de las aplicaciones como un usuario estándar.

Para obtener información acerca de UAC, vea los temas siguientes.



| Tema                                                                                                                                        | Descripción                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Instrucciones para el control de cuentas de usuario en el desarrollo de la interfaz de usuario](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Información general acerca de UAC.<br/>                                                                                                     |
| [Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelos para desarrollar aplicaciones que realizan operaciones que requieren privilegios administrativos, pero que se ejecutan como un usuario estándar.<br/> |
| [Referencia de autorización](authorization-reference.md)<br/>                                                                            | Información detallada sobre las funciones de autorización, las interfaces, las estructuras y otros elementos de programación.<br/>                        |



 

 

 




