---
description: En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver los resultados de la búsqueda en RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conexión del servicio Web en la búsqueda federada de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153976"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Conexión del servicio Web en la búsqueda federada de Windows

En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver los resultados de la búsqueda en RSS o Atom.

Este tema se organiza de la siguiente manera:

-   [Conexión del servicio Web](#connect-your-web-service)
-   [Registrar un almacén de datos remoto existente](#register-an-existing-remote-data-store)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="connect-your-web-service"></a>Conexión del servicio Web

**Para conectar el servicio Web del almacén de datos a la búsqueda federada, realice los pasos siguientes:**

1.  Cree un archivo. osdx.
2.  Proporcione el archivo. osdx a los usuarios para que puedan agregar el servicio a petición abriendo el archivo. osdx.
3.  Genere un conector de búsqueda e impleméntelo activamente en su empresa.

## <a name="register-an-existing-remote-data-store"></a>Registrar un almacén de datos remoto existente

Un usuario registra un nuevo almacén de datos remoto con la búsqueda federada de Windows abriendo un archivo de descripción de OpenSearch (. osdx). Cuando el usuario lo hace, se producen los siguientes eventos:

1.  Se crea un archivo. searchconnector-MS (conector de búsqueda) en la carpeta búsquedas de Windows (% userprofile%/searches).
2.  Se crea un acceso directo al archivo. searchconnector-MS en la carpeta links (% userprofile%/links).
3.  Aparece un acceso directo en el panel **Favoritos** de navegación del explorador de Windows, lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio Web.

> [!Note]  
> Un almacén de datos que ya tiene un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) compatible con la búsqueda federada de Windows se puede Agregar al explorador de Windows cuando un usuario abre un archivo. osdx.

 

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introducción con búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Siguientes procedimientos recomendados en la búsqueda federada de Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
