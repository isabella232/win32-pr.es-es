---
title: Archivos generados para una interfaz COM
description: En el caso de las interfaces COM, el compilador MIDL combina todas las rutinas y datos auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL del compilador MIDL, MIDL y COM
- MIDL EN COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995179"
---
# <a name="files-generated-for-a-com-interface"></a>Archivos generados para una interfaz COM

En el caso de las interfaces COM, el compilador MIDL combina todas las rutinas y datos auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz. Este archivo incluye los puntos de entrada suplente para clientes y servidores. Además, el compilador MIDL genera un archivo de encabezado de interfaz, un archivo UUID de interfaz y un archivo de registro de interfaz. Usará todos estos archivos al crear un archivo DLL de proxy que contenga el código para admitir el uso de la interfaz por parte de las aplicaciones cliente y los servidores de objetos. También usará el archivo de encabezado de interfaz y el archivo UUID de interfaz al crear el archivo ejecutable para una aplicación cliente que use la interfaz.

En los temas siguientes se describe cada uno de los archivos generados para una interfaz COM personalizada, que se identifican mediante la inclusión del **\[** [](object.md) **\]** atributo de objeto en la lista de atributos de interfaz del archivo IDL:

-   [El archivo de proxy de interfaz](the-interface-proxy-file.md)
-   [Archivos de encabezado](the-header-files.md)
-   [El archivo UUID de la interfaz](the-interface-uuid-file.md)
-   [El archivo de registro de la interfaz](the-interface-registration-file.md)

Para obtener más información, consulte archivo de configuración de la [aplicación (ACF)](application-configuration-file-acf-.md), [**/App \_ config**](-app-config.md), [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)y [compilar y registrar un archivo dll de proxy](../com/building-and-registering-a-proxy-dll.md).

 

 