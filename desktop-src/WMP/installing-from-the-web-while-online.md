---
title: Instalación desde la web mientras está en línea
description: Instalación desde la web mientras está en línea
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Reproductor de Windows Media en línea, instalar desde web mientras está en línea
- online stores,installing from Web while online
- tiendas en línea de tipo 1, instalar desde La Web mientras está en línea
- tiendas en línea de tipo 2, instalar desde La Web mientras está en línea
- Reproductor de Windows Media en línea, instalación en línea desde Web
- online stores,online installs from Web
- tiendas en línea de tipo 1, instalación en línea desde Web
- tiendas en línea de tipo 2, instalación en línea desde Web
- instalar tiendas en línea desde La Web mientras está en línea
- instalación en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801dd9fbee8bff2660a39f6b40e8a5a9e703df00f82be54a7b93c0d200d2ccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135558"
---
# <a name="installing-from-the-web-while-online"></a>Instalación desde la web mientras está en línea

Los usuarios pueden instalar Reproductor de Windows Media como una descarga web mientras están conectados a Internet. En este caso, Microsoft puede configurar la tienda en línea inicial que especifique.

Para redistribuir Reproductor de Windows Media de esta manera, use la siguiente dirección URL:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*

En la dirección URL anterior, establezca *key* en el nombre de clave del almacén en línea y *establezca localeID* en el identificador de la configuración regional donde el almacén proporciona el servicio. Establezca *la* versión en 2 para Reproductor de Windows Media 11 en Windows XP o 1 para Reproductor de Windows Media 10. La dirección URL Reproductor de Windows Media y establece el almacén activo inicial en el especificado por *la clave*.

En el ejemplo siguiente se muestra una dirección URL que Reproductor de Windows Media 11 y establece Proseware como almacén activo inicial. El valor 409 para *localeID* indica que Proseware proporciona servicio en el Estados Unidos.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Si el documento ServiceInfo de la tienda en línea incluye un elemento Install, Reproductor de Windows Media el programa de instalación personalizará el proceso de instalación. Con los valores de atributo, el programa de instalación muestra el Contrato de licencia del usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo .cab en el equipo del usuario. Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




