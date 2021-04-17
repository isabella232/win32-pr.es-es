---
title: IDENTIFICADOR de clave y clave
description: IDENTIFICADOR de clave y clave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- Administración de derechos digitales (DRM), claves
- DRM (administración de derechos digitales), claves
- Administración de derechos digitales (DRM), KID
- DRM (administración de derechos digitales), KID
- IDENTIFICADOR de clave (KID)
- KID (identificador de clave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704635"
---
# <a name="key-and-key-id"></a>IDENTIFICADOR de clave y clave

Al empaquetar un archivo, se usa una clave. Una clave es un fragmento de datos que se usa en los algoritmos de cifrado que protegen el contenido. Hay dos partes en cada clave: una inicialización de clave de licencia y un identificador de clave (a menudo abreviado como KID). El identificador de clave es público y se almacena en el encabezado de archivo como una manera de identificar la clave necesaria para descifrar el archivo. La inicialización de la clave de licencia es un valor secreto que debe compartir el Empaquetador de contenido y el emisor de la licencia.

Un identificador de clave identifica el contenido protegido desde la perspectiva de la licencia. Aunque puede usar el mismo identificador de clave para varios archivos, se recomienda usar siempre un identificador de clave único para cada fragmento de contenido protegido.

Muchos de los métodos descritos en esta documentación usan cadenas de identificador de clave para seleccionar licencias. Estas cadenas contienen el identificador de clave codificado en Base64.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




