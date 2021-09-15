---
description: Solucionador de origen
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Solucionador de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574756"
---
# <a name="source-resolver"></a>Solucionador de origen

La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión. La resolución del origen es la forma estándar que tienen las aplicaciones para crear los orígenes multimedia.

Internamente, el solucionador de origen usa *objetos de* controlador:

-   *Los controladores de esquema* toman una dirección URL y crean un origen multimedia o una secuencia de bytes.
-   *Los controladores de flujo de bytes* toman una secuencia de bytes y crean un origen multimedia.

Puede implementar un controlador personalizado y agregarlo al Registro. Los controladores de esquema se registran por esquema de dirección URL y los controladores de secuencias de bytes se registran mediante la extensión de nombre de archivo o el tipo MIME.

Este tema contiene las siguientes secciones:

-   [Usar el solucionador de origen](using-the-source-resolver.md)
-   [Configuración de un origen multimedia](configuring-a-media-source.md)
-   [Controladores de esquema y Byte-Stream controladores de esquema](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> </dl>

 

 



