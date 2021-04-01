---
title: Parámetros de la línea de comandos del programa de instalación para tiendas en línea
description: Parámetros de la línea de comandos del programa de instalación para tiendas en línea
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player tiendas en línea, parámetros de la línea de comandos del programa de instalación
- tiendas en línea, parámetros de la línea de comandos del programa de instalación
- Escriba 1 tiendas en línea, parámetros de la línea de comandos del programa de instalación
- tipo 2 tiendas en línea, parámetros de la línea de comandos del programa de instalación
- parámetros de la línea de comandos del programa de instalación
- Windows Media Player tiendas en línea, parámetros de la línea de comandos
- tiendas en línea, parámetros de la línea de comandos
- tipo 1 almacenes en línea, parámetros de la línea de comandos
- tipo 2 tiendas en línea, parámetros de la línea de comandos
- parámetros de la línea de comandos
- Windows Media Player tiendas en línea, parámetros
- tiendas en línea, parámetros
- tipo 1 tiendas en línea, parámetros
- tipo 2 tiendas en línea, parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075655"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Parámetros de la línea de comandos del programa de instalación para tiendas en línea

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Al instalar Windows Media Player 10 o Windows Media Player 11 en Windows XP, puede anexar parámetros de la línea de comandos para especificar la primera tienda en línea que el usuario ve.

Sintaxis


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parámetros

DefaultService (obligatorio)

Nombre de clave de la tienda en línea. Este valor debe coincidir con el nombre de clave del atributo **clave** del elemento **ServiceInfo** del documento serviceinfo.

ServiceInfo (obligatorio)

La ruta de acceso completa a un documento ServiceInfo instalado en el equipo del usuario.

ServiceExtra (opcional)

Cadena de consulta que Windows Media Player 10 anexará a la dirección URL del documento ServiceInfo cuando recupere el documento en línea.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de cómo redistribuir el software de Windows Media Player con su aplicación, consulte [redistribuir el software de windows media Player](redistributing-windows-media-player-software.md).

Cuando el equipo del usuario no está conectado a Internet, la información contenida en el documento ServiceInfo local se usa para configurar Windows Media Player para el servicio activo inicial.

Los parámetros de línea de comandos distinguen mayúsculas de minúsculas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tiendas en línea con personalización de marca**](co-branding-online-stores.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




