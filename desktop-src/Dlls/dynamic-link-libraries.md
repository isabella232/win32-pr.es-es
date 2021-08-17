---
description: Una biblioteca de vínculos dinámicos (DLL) es un módulo que contiene funciones y datos que otro módulo (aplicación o DLL) puede usar.
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link bibliotecas (bibliotecas de vínculos dinámicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369091464aad63ea78ea9f24a84fb4eb49eb810a1faff14571fc67e2e39bb0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815904"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link bibliotecas (bibliotecas de vínculos dinámicos)

Una *biblioteca de vínculos dinámicos* (DLL) es un módulo que contiene funciones y datos que otro módulo (aplicación o DLL) puede usar.

Un archivo DLL puede definir dos tipos de funciones: exportadas e internas. Las funciones exportadas están diseñadas para ser llamadas por otros módulos, así como desde el archivo DLL donde se definen. Normalmente, las funciones internas están diseñadas para llamarse solo desde el archivo DLL donde se definen. Aunque un archivo DLL puede exportar datos, sus datos suelen usarse solo por sus funciones. Sin embargo, no hay nada que impida que otro módulo lea o escriba esa dirección.

Los archivos DLL proporcionan una manera de modularizar las aplicaciones para que su funcionalidad se pueda actualizar y reutilizar más fácilmente. Los archivos DLL también ayudan a reducir la sobrecarga de memoria cuando varias aplicaciones usan la misma funcionalidad al mismo tiempo, ya que aunque cada aplicación recibe su propia copia de los datos DLL, las aplicaciones comparten el código DLL.

La Windows de programación de aplicaciones (API) se implementa como un conjunto de archivos DLL, por lo que cualquier proceso que use la API de Windows usa la vinculación dinámica.

-   [Acerca de Dynamic-Link bibliotecas](about-dynamic-link-libraries.md)
-   [Uso de Dynamic-Link bibliotecas](using-dynamic-link-libraries.md)
-   [Referencia de la biblioteca de vínculos dinámicos](dynamic-link-library-reference.md)

> [!Note]  
> Si es un usuario que tiene dificultades con un archivo DLL en el equipo, debe ponerse en contacto con el servicio de soporte al cliente para el proveedor de software que publica el archivo DLL. Si cree que necesita soporte técnico para un producto de Microsoft (incluido Windows), vaya a nuestro sitio de soporte técnico en [support.microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ARCHIVOS DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
