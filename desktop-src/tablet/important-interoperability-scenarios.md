---
description: 'Para que una aplicación de Tablet PC funcione con la entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Escenarios de interoperabilidad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648175"
---
# <a name="important-interoperability-scenarios"></a>Escenarios de interoperabilidad importantes

Para que una aplicación de Tablet PC funcione con la entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:

-   Guarde un documento en el formato binario nativo de la aplicación sin perder la tinta del documento.
-   Guardar un documento en cualquier formato que la aplicación admita normalmente (por ejemplo, HTML o formato de texto enriquecido (RTF)) sin perder la tinta del documento.
-   Copiar la entrada manuscrita de una aplicación a otra mediante el portapapeles. Esto funciona si la otra aplicación solo reconoce un formato específico, como HTML, RTF o mapa de bits (BMP). También funciona si la aplicación de destino reconoce la tinta. Si reconoce la tinta, la aplicación de destino puede interpretar la tinta que se ha copiado como tinta y no solo como una imagen.
-   Copiar la entrada manuscrita, junto con el texto, entre dos aplicaciones que reconocen la tinta, cada una de las cuales tiene más de un objeto de [**entrada de lápiz**](inkdisp-class.md) . Esto requiere HTML, RTF o un formato similar.
-   Copie la entrada manuscrita entre dos aplicaciones, cada una de las cuales tiene un objeto de [**entrada manuscrita**](inkdisp-class.md) . El formato serializado de tinta (ISF) es suficiente para esto.
-   Copiar la entrada manuscrita de una aplicación que tiene más de un objeto de [**entrada de lápiz**](inkdisp-class.md) en una aplicación que solo tiene un objeto de **entrada manuscrita** . En este caso, la aplicación que tiene más de un objeto de **entrada de lápiz** debe ser capaz de generar el formato serializado de tinta (ISF).
-   Copiar la entrada manuscrita de una aplicación que tiene un objeto de [**entrada manuscrita**](inkdisp-class.md) en una aplicación que tiene más de un objeto de **entrada manuscrita** . En este caso, la aplicación que tiene más de un objeto de **entrada de lápiz** debe ser capaz de reconocer el ISF.

 

 



