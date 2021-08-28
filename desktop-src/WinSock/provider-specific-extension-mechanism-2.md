---
description: La función WSAIoctl permite a los proveedores de servicios ofrecer extensiones de características específicas del proveedor.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733575"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific de extensión

La [**función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite a los proveedores de servicios ofrecer extensiones de características específicas del proveedor. Este mecanismo supone, por supuesto, que una aplicación es consciente de una extensión determinada y entiende la semántica y la sintaxis implicadas. Esta información la proporcionaría normalmente el proveedor del proveedor de servicios.

Para invocar una función de extensión, la aplicación debe pedir primero un puntero a la función deseada. Esto se realiza a través de la [**función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mediante el código de comando \_ SIO GET \_ EXTENSION FUNCTION \_ \_ POINTER. El búfer de entrada para **WSAIoctl contiene** un identificador para la función de extensión deseada, mientras que el búfer de salida contiene el propio puntero de función. A continuación, la aplicación puede invocar la función de extensión directamente sin pasar por el32.dll \_ Ws2.

Los identificadores asignados a las funciones de extensión son identificadores únicos globales (GUID) asignados por proveedores de proveedores de servicios. Los proveedores que crean funciones de extensión se animan a publicar detalles completos sobre la función, incluida la sintaxis del prototipo de función. Esto permite que más de un proveedor de servicios pueda ofrecer funciones de extensión comunes y populares. Una aplicación puede obtener el puntero de función y usar la función sin necesidad de saber nada sobre el proveedor de servicios concreto que implementa la función.

En Windows Vista y versiones posteriores, las nuevas extensiones del sistema Winsock se exportan directamente desde el archivo DLL de Winsock, por lo que la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) no es necesaria para cargar estas extensiones. Las nuevas funciones de extensión disponibles en Windows Vista y versiones posteriores incluyen las funciones [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) y [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) que se exportan desde *Ws2 \_32.dll*.

 

 
