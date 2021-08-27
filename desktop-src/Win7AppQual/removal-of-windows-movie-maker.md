---
description: Eliminación de Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Eliminación de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098525"
---
# <a name="removal-of-windows-movie-maker"></a>Eliminación de Windows Movie Maker

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** alta  
**Frecuencia:** media  


## <a name="description"></a>Descripción

Microsoft está desusando y quitando la utilidad Windows Movie Maker cliente. Esto incluye:

-   Todos los puntos de entrada Windows Movie Maker (por ejemplo, menú Inicio, Iniciar > Ejecutar)
-   Todos los archivos binarios usados por Windows Movie Maker (todo lo que estaba en %ProgramFiles% \\ Movie Maker)

Sin embargo, los archivos de proyecto Movie Maker usuario permanecerán en el sistema y serán accesibles para otras aplicaciones que admitan este formato de archivo.

## <a name="manifestation"></a>Manifestación

La eliminación Windows Movie Maker da como resultado lo siguiente:

-   Cualquier intento de iniciar Windows Movie Maker con sus argumentos de línea de comandos producirá un error
-   Los complementos que se instalaron para habilitar nuevas transformaciones y animaciones permanecerán instalados, pero no se exponen al usuario final.

## <a name="solution"></a>Solución

Para tener dicha funcionalidad en el futuro, un usuario deberá instalar una aplicación similar de Microsoft u otro proveedor de software.

 

 



