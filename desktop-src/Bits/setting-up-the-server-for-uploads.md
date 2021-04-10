---
title: Configuración del servidor para cargas
description: Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI. Para conocer los requisitos de IIS, consulte requisitos de IIS para cargas de BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268315"
---
# <a name="setting-up-the-server-for-uploads"></a>Configuración del servidor para cargas

Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI. Para conocer los requisitos de IIS, consulte [requisitos de IIS para cargas de bits](iis-requirements-for-bits-uploads.md).

Para obtener información sobre la configuración del directorio virtual de IIS que usa BITS para cargas, vea los temas siguientes.

-   [Establecimiento de permisos en directorios virtuales](setting-permissions-on-virtual-directories.md)
-   [Escritura de un script para configurar el directorio virtual](writing-a-script-to-configure-the-virtual-directory.md)
-   [Usar la interfaz de usuario de IIS para configurar el directorio virtual](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Impedir varias cargas](preventing-multiple-uploads.md)
-   [Procedimientos recomendados de carga](upload-best-practices.md)

> [!Note]  
> Algunas instalaciones de IIS incluyen el componente de filtrado UrlScan. Si UrlScan está habilitado, el administrador debe agregar el verbo "BITS \_ post" a la lista de verbos http permitidos de URLScan. De lo contrario, se producirá un error en las cargas del cliente de BITS. Para obtener más información sobre cómo habilitar verbos en UrlScan, vea la documentación de UrlScan.

 

 

 




