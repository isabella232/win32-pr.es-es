---
description: En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (. osdx), cómo implementar un archivo. osdx y cómo realizar un seguimiento del uso del servicio de OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implementación de conectores de búsqueda en Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497081"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Implementación de conectores de búsqueda en la búsqueda federada de Windows

En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (. osdx), cómo implementar un archivo. osdx y cómo realizar un seguimiento del uso del servicio de [OpenSearch](https://github.com/dewitt/opensearch) .

Este tema se organiza de la siguiente manera:

-   [El archivo. searchconnector-MS (conector de búsqueda)](#the-searchconnector-ms-search-connector-file)
-   [Métodos de implementación](#deployment-methods)
    -   [Implementación de extracción](#pull-deployment)
    -   [Implementación de extracción](#push-deployment)
-   [Seguimiento del uso](#tracking-usage)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>El archivo. searchconnector-MS (conector de búsqueda)

Simplemente abrir el archivo. osdx que describe cómo conectarse al servicio Web y cómo asignar cualquier elemento personalizado en el XML de RSS o Atom registra el nuevo almacén de datos remotos con la búsqueda federada. Un almacén de datos que ya tiene un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) compatible con búsqueda federada se puede Agregar al explorador de Windows cuando un usuario abre un archivo. osdx.

Una vez que haya dado el archivo. osdx a su usuario y el usuario abra el archivo. osdx, se producirán los siguientes eventos.

1.  Se crea un archivo. searchconnector-MS en la carpeta **búsquedas de Windows** (% userprofile%/searches).
2.  Se crea un acceso directo al archivo. searchconnector-MS en la carpeta **Links** (% userprofile%/links).
3.  Aparece un acceso directo en el panel **Favoritos** de navegación del explorador de Windows, lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio Web.

## <a name="deployment-methods"></a>Métodos de implementación

Hay dos maneras de implementar conectores de búsqueda: implementación de extracción e implementación de inserción.

### <a name="pull-deployment"></a>Implementación de extracción

La implementación de extracción describe cualquier tipo de implementación en la que el usuario final toma la iniciativa para instalar los conectores de búsqueda. Los métodos comunes de implementación de extracción son:

-   Adjuntar el archivo. osdx en un correo electrónico.
-   Publicar el archivo en una página web.
-   Proporcionar un vínculo dinámico en el sitio de la intranet; por ejemplo, uno que genera archivos. osdx personalizados basados en las opciones del usuario o en el ámbito actual dentro del sitio.

Para que el archivo se descargue cuando el usuario hace clic en el vínculo en el explorador, el servidor Web que hospeda el servicio Web debe estar configurado para proporcionar el archivo. osdx como un archivo. Por lo tanto, debe configurar los tipos MIME en el servidor web para tratar los archivos. osdx como `"application/opensearchdescription+xml"` . Opcionalmente, puede usar el icono proporcionado por Microsoft para identificar el vínculo del conector de búsqueda.

### <a name="push-deployment"></a>Implementación de extracción

La implementación de inserciones describe cualquier tipo de implementación que no dependa de la iniciativa del usuario para instalar los conectores de búsqueda. Los métodos comunes de implementación de la instalación de extracción son:

-   Preferencias de directiva de grupo (GPP)
-   Script de inicio de sesión
-   Perfiles móviles
-   Creación de imágenes

## <a name="tracking-usage"></a>Seguimiento del uso

Para realizar un seguimiento del uso del servicio de [OpenSearch](https://github.com/dewitt/opensearch) por los usuarios que buscan en el explorador de Windows, filtre los archivos de registro del servidor web para esta cadena de agente de usuario: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introducción con búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Siguientes procedimientos recomendados en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> </dl>

 

 
