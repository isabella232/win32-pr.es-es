---
description: .
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Eliminación de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a3336421ae2bde761aa1d4f238b5cd135ba64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649227"
---
# <a name="removal-of-windows-movie-maker"></a>Eliminación de Windows Movie Maker

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** alta  
**Frecuencia** : medio  


## <a name="description"></a>Descripción

Microsoft está dejando de usar y quitando la utilidad Windows Movie Maker. Esto incluye:

-   Todos los puntos de entrada a Windows Movie Maker (por ejemplo, menú Inicio, Inicio > ejecutar)
-   Todos los archivos binarios usados por Windows Movie Maker (todo lo que se encontraba en% ProgramFiles% \\ Movie Maker)

Sin embargo, los archivos de proyecto de Movie Maker de un usuario permanecerán en el sistema y estarán accesibles para otras aplicaciones que admiten este formato de archivo.

## <a name="manifestation"></a>Manifestación

Quitar de Windows Movie Maker da como resultado lo siguiente:

-   Cualquier intento de iniciar Windows Movie Maker con sus argumentos de línea de comandos producirá un error
-   Los complementos que se instalaron para habilitar nuevas transformaciones y animaciones permanecerán instalados, pero no se expondrán al usuario final.

## <a name="solution"></a>Solución

Para disponer de esta funcionalidad en el futuro, el usuario deberá instalar una aplicación similar de Microsoft u otro proveedor de software.

 

 



