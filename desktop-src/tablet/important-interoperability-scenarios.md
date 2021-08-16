---
description: 'Para que una aplicación de Tablet PC funcione con entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Escenarios de interoperabilidad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42f021cd1a8dbb3a8b65780b71db66a4c43fa18097f967f794c1a2b2c3ce16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718964"
---
# <a name="important-interoperability-scenarios"></a>Escenarios de interoperabilidad importantes

Para que una aplicación de Tablet PC funcione con entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:

-   Guarde un documento en el formato binario nativo de la aplicación sin perder la entrada de lápiz del documento.
-   Guarde un documento en cualquier formato que la aplicación admita normalmente (por ejemplo, HTML o formato de texto enriquecido (RTF)) sin perder la entrada de lápiz del documento.
-   Copie la entrada de lápiz de una aplicación a otra mediante el Portapapeles. Esto funciona si la otra aplicación solo reconoce un formato específico, como HTML, RTF o mapa de bits (BMP). También funciona si la aplicación de destino reconoce la entrada de lápiz. Si reconoce la entrada de lápiz, la aplicación de destino puede interpretar la entrada de lápiz que se ha copiado como entrada manuscrita y no solo como imagen.
-   Copie la entrada de lápiz, junto con el texto, entre dos aplicaciones que reconocen la entrada de lápiz, cada una de las cuales tiene más de un objeto [**Ink.**](inkdisp-class.md) Esto requiere HTML, RTF o un formato similar.
-   Copie la entrada de lápiz entre dos aplicaciones, cada una de las cuales tiene un [**objeto Ink.**](inkdisp-class.md) Ink Serialized Format (ISF) es suficiente para esto.
-   Copie la entrada de lápiz de una aplicación que tenga más de un objeto [**Ink**](inkdisp-class.md) en una aplicación que solo tenga un **objeto Ink.** En este caso, la aplicación que tiene más de un objeto **Ink** debe ser capaz de generar Ink Serialized Format (ISF).
-   Copie la entrada de lápiz de una aplicación que tenga un [**objeto Ink**](inkdisp-class.md) en una aplicación que tenga más de un **objeto Ink.** En este caso, la aplicación que tiene más de un objeto **Ink** debe ser capaz de reconocer ISF.

 

 



