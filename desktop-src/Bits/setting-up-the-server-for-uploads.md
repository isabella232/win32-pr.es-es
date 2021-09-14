---
title: Configuración del servidor para cargas
description: Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI. Para los requisitos de IIS, vea Requisitos de IIS para cargas de BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061580"
---
# <a name="setting-up-the-server-for-uploads"></a>Configuración del servidor para cargas

Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI. Para los requisitos de IIS, vea [Requisitos de IIS para cargas de BITS.](iis-requirements-for-bits-uploads.md)

Para obtener información sobre cómo configurar el directorio virtual de IIS que BITS usa para las cargas, vea los temas siguientes.

-   [Establecer permisos en directorios virtuales](setting-permissions-on-virtual-directories.md)
-   [Escribir un script para configurar el directorio virtual](writing-a-script-to-configure-the-virtual-directory.md)
-   [Uso de la interfaz de usuario de IIS para configurar el directorio virtual](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Impedir varias cargas](preventing-multiple-uploads.md)
-   [Upload Procedimientos recomendados](upload-best-practices.md)

> [!Note]  
> Algunas instalaciones de IIS incluyen el componente de filtrado UrlScan. Si UrlScan está habilitado, el administrador debe agregar el verbo "BITS POST" a la lista de \_ verbos HTTP permitidos de UrlScan. De lo contrario, se producirá un error en las cargas de cliente de BITS. Para más información sobre cómo habilitar verbos en UrlScan, consulte la documentación de UrlScan.

 

 

 




