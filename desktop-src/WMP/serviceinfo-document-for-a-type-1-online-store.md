---
title: Documento ServiceInfo para una tienda en línea de tipo 1
description: Documento ServiceInfo para una tienda en línea de tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075869"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Documento ServiceInfo para una tienda en línea de tipo 1

Tipo 1 las tiendas en línea deben proporcionar a Microsoft la dirección URL de un documento XML que describa la tienda en línea. Windows Media Player 11 usa este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.

El documento ServiceInfo para un almacén de tipo 1 proporciona la siguiente información a Windows Media Player:

-   Información utilizada para configurar el botón **tiendas en línea** (también denominado pestaña), como el texto del botón, el color del botón y la información sobre herramientas del botón.
-   Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.
-   Dirección URL donde Windows Media Player puede recuperar el complemento de la tienda en línea para que el complemento se pueda instalar en el equipo del usuario.

Cuando Windows Media Player recupera el documento ServiceInfo de la web, anexa una cadena de consulta a la dirección URL. La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional y la ubicación geográfica del usuario, así como la versión de Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




