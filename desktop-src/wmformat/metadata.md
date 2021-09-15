---
title: Metadatos
description: Los metadatos, para los fines de este SDK, son información que describe un archivo ASF o el contenido del archivo.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows SDK de formato multimedia, información general sobre metadatos
- Formato de sistemas avanzados (ASF), información general sobre metadatos
- ASF (formato de sistemas avanzados), información general sobre metadatos
- metadata,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360213"
---
# <a name="metadata"></a>Metadatos

Los metadatos, para los fines de este SDK, son información que describe un archivo ASF o el contenido del archivo. La sección de encabezado de un archivo ASF contiene todos los metadatos asociados a ese archivo. Los elementos individuales de metadatos de un archivo ASF se denominan atributos. Cada atributo tiene un nombre y un valor. En esta documentación, se usan constantes globales para identificar atributos. Por ejemplo, el título de un archivo ASF se almacena en el **atributo g \_ wszWMTitle.**

Se definen varios atributos en el SDK Windows Media Format para controlar las necesidades de metadatos más comunes. Además, puede crear sus propios atributos. Sin embargo, debe tener cuidado al asignar nombres a los atributos personalizados, ya que otros desarrolladores de aplicaciones pueden usar los mismos nombres y pueden producirse conflictos.

El SDK establece algunos atributos y no se pueden cambiar manualmente. Por ejemplo, al indexar un archivo ASF, el SDK establece el atributo **\_ g wszWMSeekable** para mostrar que el archivo ahora se puede leer desde cualquier punto especificado.

Otros atributos son puramente informativos y deben establecerse manualmente. Por ejemplo, si desea realizar un seguimiento del autor de un archivo, debe establecer **g \_ wszWMAuthor**.

El SDK Windows Media Format proporciona compatibilidad con atributos que se aplican a todo el archivo y atributos que se aplican a secuencias individuales.

Puede usar el SDK de Windows Media Format para editar los metadatos en archivos MP3, aunque siempre debe usar atributos compatibles con ID3 en archivos MP3 para mantener la compatibilidad con otros programas de manipulación mp3.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Objeto del editor de metadatos**](metadata-editor-object.md)
</dt> <dt>

[**Características de metadatos**](metadata-features.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




