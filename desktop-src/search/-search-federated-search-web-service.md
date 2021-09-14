---
description: En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver resultados de búsqueda en RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conexión del servicio web en Windows búsqueda federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363255"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Conexión del servicio web en Windows búsqueda federada

En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver resultados de búsqueda en RSS o Atom.

Este tema se organiza de la siguiente manera:

-   [Conectar Su servicio web](#connect-your-web-service)
-   [Registro de un almacén de datos remoto existente](#register-an-existing-remote-data-store)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="connect-your-web-service"></a>Conectar Su servicio web

**Para conectar el servicio web del almacén de datos a la búsqueda federada, realice los pasos siguientes:**

1.  Cree un archivo .osdx.
2.  Proporcione el archivo .osdx a los usuarios para que puedan agregar el servicio a petición abriendo el archivo .osdx.
3.  Genere un conector de búsqueda e impleméntelo activamente en su empresa.

## <a name="register-an-existing-remote-data-store"></a>Registro de un almacén de datos remoto existente

Un usuario registra un nuevo almacén de datos remoto con Windows búsqueda federada abriendo un archivo OpenSearch description (.osdx). Cuando el usuario lo hace, se producen los siguientes eventos:

1.  Se crea un archivo .searchconnector-ms (conector de búsqueda) en la carpeta Windows Searches (%userprofile%/Searches).
2.  Se crea un acceso directo al archivo .searchconnector-ms en la carpeta Vínculos (%userprofile%/Links).
3.  Aparece un acceso directo en el panel de navegación Windows Explorer **favoritos,** lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio web.

> [!Note]  
> Un almacén de datos que ya tiene un servicio [web](https://github.com/dewitt/opensearch) OpenSearch compatible con la búsqueda federada de Windows se puede agregar a Windows Explorer cuando un usuario abre un archivo .osdx.

 

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Tareas iniciales con la búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Habilitación del almacén de datos en Windows búsqueda federada](-search-federated-search-data-store.md)
</dt> <dt>

[Crear un archivo OpenSearch descripción en Windows búsqueda federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedimientos recomendados siguientes en Windows búsqueda federada](-search-fedsearch-best.md)
</dt> <dt>

[Implementación de conectores de búsqueda en Windows búsqueda federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
