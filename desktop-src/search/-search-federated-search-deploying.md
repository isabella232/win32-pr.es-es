---
description: En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (.osdx), cómo implementar un archivo .osdx y cómo realizar un seguimiento del uso del servicio OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implementación de conectores de búsqueda Windows búsqueda federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7515fa905abf3767696457f30a52abdb0a36d78883e9649cb2bf42e77e8b8c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463141"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Implementación de conectores de búsqueda en Windows búsqueda federada

En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (.osdx), cómo implementar un archivo .osdx y cómo realizar un seguimiento del uso del servicio [OpenSearch.](https://github.com/dewitt/opensearch)

Este tema se organiza de la siguiente manera:

-   [Archivo .searchconnector-ms (Conector de búsqueda)](#the-searchconnector-ms-search-connector-file)
-   [Métodos de implementación](#deployment-methods)
    -   [Implementación de extracción](#pull-deployment)
    -   [Implementación de inserción](#push-deployment)
-   [Seguimiento del uso](#tracking-usage)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Archivo .searchconnector-ms (Conector de búsqueda)

Simplemente abrir el archivo .osdx que describe cómo conectarse al servicio web y cómo asignar elementos personalizados en RSS o Atom XML registra el nuevo almacén de datos remoto con búsqueda federada. Un almacén de datos que ya tiene un servicio web OpenSearch compatible con la búsqueda federada se puede agregar [a](https://github.com/dewitt/opensearch) Windows Explorer cuando un usuario abre un archivo .osdx.

Después de haber dado el archivo .osdx al usuario y de que el usuario abra el archivo .osdx, se producirán los siguientes eventos.

1.  Se crea un archivo .searchconnector-ms en la **carpeta Windows Búsquedas** (%userprofile%/Searches).
2.  Se crea un acceso directo al archivo .searchconnector-ms en la carpeta **Vínculos** (%userprofile%/Links).
3.  Aparece un acceso directo en el panel de navegación Windows Explorer **favoritos,** lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio web.

## <a name="deployment-methods"></a>Métodos de implementación

Hay dos maneras de implementar conectores de búsqueda, implementación de extracción e implementación de inserción.

### <a name="pull-deployment"></a>Implementación de extracción

Implementación de extracción describe cualquier tipo de implementación en la que el usuario final toma la iniciativa de instalar los conectores de búsqueda. Los métodos comunes de implementación de extracción son:

-   Adjuntar el archivo .osdx en un correo electrónico.
-   Publicar el archivo en una página web.
-   Proporcionar un vínculo dinámico en el sitio de intranet; por ejemplo, uno que genera archivos .osdx personalizados en función de las opciones del usuario o el ámbito actual dentro del sitio.

Para que el archivo se descargue cuando el usuario haga clic en el vínculo en su explorador, el servidor web que hospeda el servicio web debe configurarse para entregar el archivo .osdx como un archivo. Por lo tanto, debe configurar los tipos MIME en el servidor web para tratar los archivos .osdx como `"application/opensearchdescription+xml"` . Opcionalmente, puede usar el icono proporcionado por Microsoft para identificar el vínculo del conector de búsqueda.

### <a name="push-deployment"></a>Implementación de inserción

La implementación de inserción describe cualquier tipo de implementación que no dependa de la iniciativa del usuario para instalar los conectores de búsqueda. Los métodos comunes de implementación de inserción son:

-   directiva de grupo preferencias (GPP)
-   Script de inicio de sesión
-   Perfiles móviles
-   Creación de imágenes

## <a name="tracking-usage"></a>Seguimiento del uso

Para realizar un [](https://github.com/dewitt/opensearch) seguimiento del uso del servicio OpenSearch los usuarios que buscan en Windows Explorer, filtre los archivos de registro del servidor web para esta cadena de agente de usuario: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Tareas iniciales con la búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio web en Windows búsqueda federada](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en Windows búsqueda federada](-search-federated-search-data-store.md)
</dt> <dt>

[Crear un archivo OpenSearch descripción en Windows búsqueda federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedimientos recomendados siguientes en Windows búsqueda federada](-search-fedsearch-best.md)
</dt> </dl>

 

 
