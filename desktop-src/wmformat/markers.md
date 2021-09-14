---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows SDK de formato multimedia, marcadores
- Formato de sistemas avanzados (ASF), marcadores
- ASF (formato de sistemas avanzados),marcadores
- marcadores, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267036"
---
# <a name="markers"></a>Marcadores

Los marcadores son lugares con nombre en la escala de tiempo de un archivo ASF. Cada marcador tiene un nombre y un tiempo de presentación que se asigna. Puede especificar tantos marcadores como necesite para un archivo.

Los marcadores son útiles para dividir archivos ASF grandes en partes lógicas. Una aplicación que usa el objeto de lector para reproducir archivos ASF puede proporcionar al usuario la opción de pasar del marcador al marcador, lo que simplifica la navegación de los medios digitales. Por ejemplo, si va a crear un archivo ASF fuera de una presentación, puede colocar marcadores en la escala de tiempo de cada tema principal que se describe. En la reproducción, en lugar de obtener una escala de tiempo larga y tener que adivinar en la ubicación a la que buscar, un usuario puede elegir simplemente un tema de una lista y ir directamente a la parte pertinente del archivo.

El objeto del editor de metadatos manipula los marcadores. Puede agregar, quitar y ver los marcadores de un archivo en cualquier momento después de que se haya escrito el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Para buscar marcadores**](to-seek-to-markers.md)
</dt> <dt>

[**Uso de marcadores**](using-markers.md)
</dt> </dl>

 

 




