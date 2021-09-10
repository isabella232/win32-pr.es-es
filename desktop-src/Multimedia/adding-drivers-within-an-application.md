---
title: Agregar controladores dentro de una aplicación
description: Agregar controladores dentro de una aplicación
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Administrador de compresión de audio (ACM), agregar controladores
- ACM (administrador de compresión de audio), agregar controladores
- Ejemplos de ACM, agregar controladores
- agregar controladores
- función acmDriverAdd
- controladores globales
- controladores locales
- administrador de compresión de audio (ACM), controladores globales
- ACM (administrador de compresión de audio), controladores globales
- administrador de compresión de audio (ACM), controladores locales
- ACM (administrador de compresión de audio), controladores locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370334"
---
# <a name="adding-drivers-within-an-application"></a>Agregar controladores dentro de una aplicación

Si necesita que la aplicación implemente sus propias rutinas de compresión internamente, la aplicación puede agregar controladores al ACM mediante una llamada a la función [**acmDriverAdd.**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) La aplicación implementa el controlador proporcionando una función que se ajusta [**al prototipo acmDriverProc.**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) Después de que la aplicación haya agregado el controlador, la aplicación puede usar el controlador a través del ACM como usaría con cualquier otro controlador.

El ACM trata los controladores como globales o locales. Una aplicación especifica si se debe agregar un controlador como global o local cuando llama **a acmDriverAdd**. Hay dos diferencias entre los controladores globales y locales:

-   Los controladores agregados como controladores globales no se comparten con otras aplicaciones.
-   Una aplicación puede modificar directamente la prioridad de un controlador global (pero no un controlador local) llamando a la función [**acmDriverPriority.**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) El ACM realiza una búsqueda prioritaria al buscar un controlador adecuado para proporcionar una implementación de una llamada de función. El ACM siempre da a los controladores locales una prioridad más alta que los controladores globales. El controlador local agregado más recientemente tiene la prioridad más alta.

 

 




