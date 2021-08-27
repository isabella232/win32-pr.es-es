---
title: Documento ServiceInfo para una tienda en línea de tipo 1
description: Documento ServiceInfo para una tienda en línea de tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Reproductor de Windows Media en línea,documento ServiceInfo
- online stores,ServiceInfo document
- tipo 1 tiendas en línea, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893cb3c849e062147d0f6bc80f3f9c1bd56a3457b60dfe30ce837820091e9710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995445"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Documento ServiceInfo para una tienda en línea de tipo 1

Las tiendas en línea de tipo 1 deben proporcionar a Microsoft la dirección URL de un documento XML que describa la tienda en línea. Reproductor de Windows Media 11 usa este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.

El documento ServiceInfo de un almacén de tipo 1 proporciona la siguiente información para Reproductor de Windows Media:

-   Información utilizada para configurar el botón **Tiendas** en línea (también denominada pestaña), como el texto del botón, el color del botón y la información sobre herramientas del botón.
-   Direcciones URL de las imágenes que Reproductor de Windows Media muestran para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Reproductor de Windows Media hosts en su interfaz de usuario.
-   Dirección URL Reproductor de Windows Media puede recuperar el complemento de la tienda en línea para que el complemento se pueda instalar en el equipo del usuario.

Cuando Reproductor de Windows Media recupera el documento ServiceInfo de la Web, anexa una cadena de consulta a la dirección URL. La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional y la ubicación geográfica del usuario, así como la versión de Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




