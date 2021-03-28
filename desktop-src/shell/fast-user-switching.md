---
description: En los sistemas operativos anteriores, era necesario que el usuario cerrara sesión antes de que otro usuario pudiera iniciar sesión. A partir de Windows XP, un usuario no tiene que cerrar sesión para permitir que otro usuario inicie sesión.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Cambio rápido de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d79f16ef8a1ea8c97bfb61d34dfa727f3d0cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997749"
---
# <a name="fast-user-switching"></a>Cambio rápido de usuario

Cuando un usuario inicia sesión en un equipo, el sistema carga su perfil. Dado que cada usuario tiene una cuenta de usuario única, permite que varios usuarios compartan un equipo. Cuando un usuario inicia sesión, la configuración del escritorio, los archivos, los favoritos y el historial que ven son los suyos; otros usuarios no pueden tener acceso a ellos. Cuando el usuario cierra la sesión, su perfil se conservará la próxima vez que inicie sesión. En los sistemas operativos anteriores, era necesario que el usuario cerrara sesión antes de que otro usuario pudiera iniciar sesión. A partir de Windows XP, un usuario no tiene que cerrar sesión para permitir que otro usuario inicie sesión. En su lugar, es posible que varios usuarios inicien sesión y cambien rápidamente entre sus cuentas abiertas. Esta característica se conoce como *cambio rápido de usuario*. Al cambiar a otra cuenta, no se cambia el estado de las aplicaciones que un usuario está ejecutando actualmente. Supongamos, por ejemplo, que un usuario permite que otro usuario cambie a su cuenta mientras el primer usuario ha iniciado sesión. Cuando el primer usuario cambia a su cuenta, se ejecutan sus aplicaciones y se conservan sus conexiones de red. Por lo tanto, parece que ambos usuarios usan el equipo simultáneamente.

Si las aplicaciones cumplen con los requisitos del logotipo de Windows 2000, deben funcionar con el cambio rápido de usuario en Windows XP y sistemas operativos posteriores. Sin embargo, es importante tener en cuenta este escenario al desarrollar una aplicación para que se comportase como cabría esperar los usuarios. Al escribir las aplicaciones, siga estas directrices:

-   Implemente una separación de perfil verdadera. El sistema proporciona una infraestructura subyacente que admite la separación de los datos de usuario, la configuración de usuario y la configuración del equipo. Por ejemplo, use la carpeta **documentos** del usuario para almacenar los datos creados por el usuario. Para buscar un directorio para los datos específicos de la aplicación, use el sistema de [carpetas conocido](known-folders.md) con [**FOLDERID \_ RoamingAppData**](knownfolderid.md)) o, en el caso de los sistemas operativos anteriores, el sistema [**CSIDL**](csidl.md) con [**CSIDL \_ AppData**](csidl.md). Use **FOLDERID \_ LocalAppData** o **CSIDL \_ local \_ AppData** para datos que no deben estar disponibles para el usuario en otros equipos, como los archivos temporales.
-   Regístrese para recibir notificaciones de un conmutador de usuario. Normalmente, no es necesario notificar a una aplicación cuando se produce el cambio. Sin embargo, si se debe notificar a la aplicación de un cambio de sesión, se puede registrar para recibir un mensaje de [**\_ \_ cambio de WM WTSSESSION**](../termserv/wm-wtssession-change.md) .
-   Tenga en cuenta otras instancias de la aplicación. Por ejemplo, hay ocasiones en las que una aplicación debe descargar una actualización de Internet. Se puede producir un error en la actualización si otro usuario está ejecutando simultáneamente una instancia de la aplicación en otra sesión. Incluso si la actualización se realiza correctamente, la actualización puede hacer que otras instancias en ejecución de la aplicación se comporten de manera imprevisible. Por lo tanto, es mejor realizar una actualización dinámica solo si no se está ejecutando ninguna otra instancia de la aplicación. Antes de descargar una actualización de la aplicación, es posible que sea adecuado implementar un método que indique todas las instancias en ejecución de la aplicación para guardar los datos y salir sin problemas.

 

 
