---
title: Co-Branding Online Stores
description: Co-Branding Online Stores
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Reproductor de Windows Media en línea, personal de marca
- tiendas en línea, personal de marca
- tiendas en línea de tipo 1, personal de marca
- tiendas en línea de tipo 2, personal de marca
- tiendas en línea de personal de marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3ca69c377a7aedeb71f05008d707fab955f02bf0e02d7b0ca35861105aade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342136"
---
# <a name="co-branding-online-stores"></a>Co-Branding Online Stores

Los OEM de equipos personales que no operan una tienda de música pueden crear marcas con proveedores de tiendas en línea. Reproductor de Windows Media configuración admite el parámetro de línea de comandos ServiceExtra para permitir que los OEM de hardware establezcan un atributo personalizado que el almacén en línea puede usar para identificar qué OEM instaló el almacén en línea inicial.

Por ejemplo, si un creador de equipos denominado Fabrikam desea establecer la tienda en línea inicial en la tienda de música de Proseware, podría usar la siguiente línea de comandos para instalar Reproductor de Windows Media 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Cuando Reproductor de Windows Media se instala de esta manera, el reproductor anexa la cadena ServiceExtra cada vez que abre el servicio Proseware. En el ejemplo siguiente se muestra la dirección URL Reproductor de Windows Media enviaría al servicio Proseware para recuperar el documento ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



A continuación, la tienda en línea de Proseware puede usar la cadena de consulta para determinar qué OEM instaló Reproductor de Windows Media y devolver un documento ServiceInfo generado dinámicamente que apunta a la versión con marca de la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Configuración de parámetros de la línea de comandos para almacenes en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




