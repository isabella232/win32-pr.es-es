---
description: Una biblioteca de vínculos dinámicos (DLL) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliotecas de Dynamic-Link (bibliotecas de vínculos dinámicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811486"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Bibliotecas de Dynamic-Link (bibliotecas de vínculos dinámicos)

Una *biblioteca de vínculos dinámicos* (dll) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o dll).

Un archivo DLL puede definir dos tipos de funciones: exportada e interna. Las funciones exportadas están diseñadas para ser llamadas por otros módulos, así como desde el archivo DLL en el que se definen. Normalmente, las funciones internas están pensadas para ser llamadas solo desde dentro del archivo DLL donde están definidas. Aunque un archivo DLL puede exportar datos, sus datos normalmente solo se usan en sus funciones. Sin embargo, no hay nada que impida que otro módulo lea o escriba esa dirección.

Los archivos dll proporcionan una manera de modularr las aplicaciones para que su funcionalidad se pueda actualizar y reutilizar más fácilmente. Los archivos dll también ayudan a reducir la sobrecarga de memoria cuando varias aplicaciones usan la misma funcionalidad al mismo tiempo, porque aunque cada aplicación recibe su propia copia de los datos de la DLL, las aplicaciones comparten el código DLL.

La interfaz de programación de aplicaciones (API) de Windows se implementa como un conjunto de archivos dll, por lo que cualquier proceso que use la API de Windows usa la vinculación dinámica.

-   [Acerca de las bibliotecas de Dynamic-Link](about-dynamic-link-libraries.md)
-   [Usar bibliotecas de Dynamic-Link](using-dynamic-link-libraries.md)
-   [Referencia de biblioteca de vínculos dinámicos](dynamic-link-library-reference.md)

> [!Note]  
> Si es un usuario que está experimentando dificultades con un archivo DLL en el equipo, debe ponerse en contacto con el servicio de soporte al cliente para el proveedor de software que publica el archivo DLL. Si cree que necesita soporte técnico para un producto de Microsoft (incluido Windows), visite el sitio de soporte técnico en [support.Microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
