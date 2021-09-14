---
title: Archivos generados para una interfaz COM
description: En el caso de las interfaces COM, el compilador MIDL combina todos los datos y rutinas auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL del compilador MIDL, MIDL y COM
- COM MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159589"
---
# <a name="files-generated-for-a-com-interface"></a>Archivos generados para una interfaz COM

En el caso de las interfaces COM, el compilador MIDL combina todos los datos y rutinas auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz. Este archivo incluye los puntos de entrada suplentes para clientes y servidores. Además, el compilador MIDL genera un archivo de encabezado de interfaz, un archivo UUID de interfaz y un archivo de registro de interfaz. Usará todos estos archivos al crear un archivo DLL de proxy que contenga el código para admitir el uso de la interfaz tanto por parte de las aplicaciones cliente como de los servidores de objetos. También usará el archivo de encabezado de interfaz y el archivo UUID de interfaz al crear el archivo ejecutable para una aplicación cliente que usa la interfaz .

En los temas siguientes se describe cada uno de los archivos generados para una interfaz COM personalizada, que se identifica mediante la inclusión del atributo object en la lista de atributos de interfaz **\[** [](object.md) **\]** del archivo IDL:

-   [El archivo de proxy de interfaz](the-interface-proxy-file.md)
-   [Los archivos de encabezado](the-header-files.md)
-   [El archivo UUID de interfaz](the-interface-uuid-file.md)
-   [El archivo de registro de interfaz](the-interface-registration-file.md)

Para obtener más información, vea Archivo de configuración de la aplicación [(ACF),](application-configuration-file-acf-.md) [**/app \_ config**](-app-config.md), Archivo de definición de [interfaz (IDL)](interface-definition-idl-file.md)y Compilar y [registrar un archivo DLL de proxy.](../com/building-and-registering-a-proxy-dll.md)

 

 