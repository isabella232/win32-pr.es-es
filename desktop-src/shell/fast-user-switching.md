---
description: En sistemas operativos anteriores, se requería que un usuario cerrara la sesión antes de que otro usuario pudiera iniciar sesión. A Windows XP, un usuario no tiene que cerrar sesión para permitir que otro usuario inicie sesión.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Cambio rápido de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ac8c8a619f715e0dd39d6df65a131bded952aa11cc4d6aef08e18c8ca20938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050273"
---
# <a name="fast-user-switching"></a>Cambio rápido de usuario

Cuando un usuario inicia sesión en un equipo, el sistema carga su perfil. Dado que cada usuario tiene una cuenta de usuario única, esto permite que varios usuarios compartan un equipo. Cuando un usuario inicia sesión, la configuración de escritorio, los archivos, los favoritos y el historial que ve son suyos. Otros usuarios no pueden acceder a ellos. Cuando ese usuario cierra la sesión, su perfil se conserva para la próxima vez que inicie sesión. En sistemas operativos anteriores, se requería que un usuario cerrara la sesión antes de que otro usuario pudiera iniciar sesión. A Windows XP, un usuario no tiene que cerrar sesión para permitir que otro usuario inicie sesión. En su lugar, es posible que varios usuarios inicien sesión y cambien rápidamente entre sus cuentas abiertas. Esta característica se conoce como cambio *rápido de usuario.* Cambiar a otra cuenta no cambia el estado de las aplicaciones que un usuario está ejecutando actualmente. Supongamos, por ejemplo, que un usuario permite a otro usuario cambiar a su cuenta mientras el primer usuario ha iniciado sesión. Cuando el primer usuario vuelve a su cuenta, sus aplicaciones se ejecutan y se conservan sus conexiones de red. Por lo tanto, parece que ambos usuarios usan simultáneamente el equipo.

Si las aplicaciones cumplen los requisitos del logotipo de Windows 2000, deben trabajar con la conmutación rápida de usuarios en Windows XP y sistemas operativos posteriores. Sin embargo, es importante tener en cuenta este escenario al desarrollar una aplicación para que se comporte como lo esperarían los usuarios. Use las siguientes directrices al escribir las aplicaciones:

-   Implemente la separación de perfiles verdadera. El sistema proporciona una infraestructura subyacente que admite la separación de los datos de usuario, la configuración de usuario y la configuración del equipo. Por ejemplo, use la carpeta **Documentos** del usuario para almacenar los datos creados por el usuario. Para buscar un directorio para datos [](known-folders.md) específicos de la aplicación, use el sistema de carpetas conocido con [**FOLDERID \_ RoamingAppData**](knownfolderid.md)) o, para sistemas operativos anteriores, el sistema [**CSIDL**](csidl.md) con [**CSIDL \_ APPDATA**](csidl.md)). Use **FOLDERID \_ LocalAppData** o **CSIDL \_ LOCAL \_ APPDATA** para los datos que no deben estar disponibles para el usuario en otros equipos, como archivos temporales.
-   Regístrese para recibir la notificación de un cambio de usuario. Normalmente, no es necesario notificar a una aplicación cuando se produce el cambio. Sin embargo, si la aplicación debe recibir una notificación de un cambio de sesión, puede registrarse para recibir un [**mensaje DE CAMBIO DE WM \_ WTSSESSION. \_**](../termserv/wm-wtssession-change.md)
-   Tenga en cuenta otras instancias de la aplicación. Por ejemplo, hay ocasiones en las que una aplicación debe descargar una actualización de Internet. La actualización puede producir un error si otro usuario ejecuta simultáneamente una instancia de la aplicación en otra sesión. Incluso si la actualización se realiza correctamente, la actualización puede hacer que otras instancias en ejecución de la aplicación se comporten de una manera impredecible. Por lo tanto, es mejor realizar una actualización dinámica solo si no se ejecuta ninguna otra instancia de la aplicación. Antes de descargar una actualización de la aplicación, puede ser adecuado implementar un método que señale a todas las instancias en ejecución de la aplicación para que guarden los datos y se cierren sin problemas.

 

 
