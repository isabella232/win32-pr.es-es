---
title: Co-Branding tiendas en línea
description: Co-Branding tiendas en línea
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player tiendas en línea, personalización de marca
- tiendas en línea, personalización de marca
- tipo 1 tiendas en línea, personalización de marca
- tipo 2 tiendas en línea, personalización de marca
- tiendas en línea con personalización de marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695310"
---
# <a name="co-branding-online-stores"></a>Co-Branding tiendas en línea

Los OEM de equipos personales que no operan una tienda de música pueden coexistir con proveedores de tiendas en línea. El programa de instalación de Windows Media Player admite el parámetro de línea de comandos ServiceExtra para permitir que los OEM de hardware establezcan un atributo personalizado que la tienda en línea pueda usar para identificar qué OEM instaló la tienda en línea inicial.

Por ejemplo, si un creador de equipo llamado Fabrikam desea establecer la tienda en línea inicial en el almacén de música de Proseware, podría usar la siguiente línea de comandos para instalar Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Cuando Windows Media Player se instala de esta manera, el reproductor anexa la cadena ServiceExtra cada vez que abre el servicio Proseware. En el ejemplo siguiente se muestra la dirección URL que Windows Media Player enviará al servicio Proseware para recuperar el documento ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



La tienda en línea de Proseware puede usar la cadena de consulta para determinar qué OEM instaló Windows Media Player y devolver un documento de ServiceInfo generado dinámicamente que apunte a la versión con personalización de marca de la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




