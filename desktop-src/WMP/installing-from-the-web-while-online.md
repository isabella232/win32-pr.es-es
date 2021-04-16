---
title: Instalación desde la web en línea
description: Instalación desde la web en línea
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player tiendas en línea, instalar desde web mientras está en línea
- tiendas en línea, instalar desde web en línea
- Escriba 1 tiendas en línea, instalación desde web mientras está en línea
- Escriba 2 tiendas en línea, instalación desde web mientras está en línea
- Windows Media Player tiendas en línea, instalaciones en línea desde web
- tiendas en línea, instalaciones en línea desde web
- tipo 1 tiendas en línea, instalaciones en línea desde web
- tipo 2 tiendas en línea, instalaciones en línea desde web
- instalación de tiendas en línea desde web en línea
- instalaciones en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685568"
---
# <a name="installing-from-the-web-while-online"></a>Instalación desde la web en línea

Los usuarios pueden instalar Windows Media Player como una descarga web mientras están conectados a Internet. En este caso, Microsoft puede configurar la tienda en línea inicial que especifique.

Para redistribuir Windows Media Player de esta manera, use la siguiente dirección URL:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*versión*&UserLocale =*localID*&servicio =*clave*

En la dirección URL anterior, establezca *clave* en el nombre de la clave de la tienda en línea y establezca *localeID* en el identificador de la configuración regional en la que el almacén proporciona el servicio. Establezca *versión* en 2 para Windows Media Player 11 en Windows XP o 1 para Windows Media Player 10. La dirección URL instala Windows Media Player y establece el almacén activo inicial en el especificado por *clave*.

En el ejemplo siguiente se muestra una dirección URL que instala Windows Media Player 11 y establece Proseware como el almacén activo inicial. El valor de 409 para *localeID* indica que Proseware proporciona el servicio en el Estados Unidos.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Si el documento ServiceInfo de la tienda en línea incluye un elemento install, el programa de instalación de Windows Media Player personalizará el proceso de instalación. Con los valores de atributo, el programa de instalación muestra el contrato de licencia para el usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo. cab en el equipo del usuario. Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




