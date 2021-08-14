---
title: Configuración de parámetros de línea de comandos para almacenes en línea
description: Configuración de parámetros de línea de comandos para almacenes en línea
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Reproductor de Windows Media en línea, configurar parámetros de línea de comandos
- online stores,setup command-line parameters
- type 1 online stores,setup command-line parameters
- type 2 online stores,setup command-line parameters
- parámetros de línea de comandos de configuración
- Reproductor de Windows Media en línea, parámetros de línea de comandos
- tiendas en línea, parámetros de línea de comandos
- type 1 online stores,command-line parameters
- tiendas en línea de tipo 2, parámetros de línea de comandos
- parámetros de la línea de comandos
- Reproductor de Windows Media online stores,parameters
- tiendas en línea, parámetros
- tipo 1 online stores,parameters
- tipo 2 tiendas en línea, parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77df581b2be4b2539772065e1aabef281a4c6c931ca115a4f6331063cf2414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569306"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Configuración de parámetros de línea de comandos para almacenes en línea

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Al instalar Reproductor de Windows Media 10 o Reproductor de Windows Media 11 en Windows XP, puede anexar parámetros de línea de comandos para especificar el primer almacén en línea que el usuario ve.

Sintaxis


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parámetros

DefaultService (obligatorio)

Nombre de clave de la tienda en línea. Este valor debe coincidir con el nombre de clave del **atributo Key** del **elemento ServiceInfo** del documento ServiceInfo.

ServiceInfo (obligatorio)

Ruta de acceso completa a un documento ServiceInfo instalado en el equipo del usuario.

ServiceExtra (opcional)

Una cadena de consulta Reproductor de Windows Media 10 se anexará a la dirección URL del documento ServiceInfo cuando recupere el documento en línea.

## <a name="remarks"></a>Comentarios

Para más información sobre cómo redistribuir Reproductor de Windows Media software con la aplicación, consulte [Redistribuir Reproductor de Windows Media Software](redistributing-windows-media-player-software.md).

Cuando el equipo del usuario no está conectado a Internet, la información contenida en el documento ServiceInfo local se usa para configurar Reproductor de Windows Media para el servicio activo inicial.

Los parámetros de la línea de comandos distinguen mayúsculas de minúsculas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Co-Branding Online Stores**](co-branding-online-stores.md)
</dt> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




