---
description: Solucionador de origen
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Solucionador de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360475"
---
# <a name="source-resolver"></a>Solucionador de origen

La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión. La resolución del origen es la forma estándar que tienen las aplicaciones para crear los orígenes multimedia.

Internamente, la resolución de origen usa objetos de *controlador* :

-   Los *controladores de esquema* toman una dirección URL y crean un origen de medios o un flujo de bytes.
-   Los *controladores de secuencias de bytes* toman una secuencia de bytes y crean un origen de medios.

Puede implementar un controlador personalizado y agregarlo al registro. Los controladores de esquema se registran mediante el esquema de direcciones URL y los controladores de secuencias de bytes se registran mediante la extensión de nombre de archivo o el tipo MIME.

Este tema contiene las siguientes secciones:

-   [Usar el solucionador de origen](using-the-source-resolver.md)
-   [Configuración de un origen de medios](configuring-a-media-source.md)
-   [Controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> </dl>

 

 



