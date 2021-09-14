---
description: Una biblioteca de vínculos dinámicos (DLL) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link bibliotecas (bibliotecas de vínculos dinámicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173745"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link bibliotecas (bibliotecas de vínculos dinámicos)

Una *biblioteca de vínculos dinámicos* (DLL) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o DLL).

Un archivo DLL puede definir dos tipos de funciones: exportadas e internas. Las funciones exportadas están diseñadas para que las llamen otros módulos, así como desde el archivo DLL donde se definen. Normalmente, las funciones internas están diseñadas para llamarse solo desde el archivo DLL donde se definen. Aunque un archivo DLL puede exportar datos, sus datos suelen usarse solo por sus funciones. Sin embargo, no hay nada que impida que otro módulo lea o escriba esa dirección.

Los archivos DLL proporcionan una manera de modularizar las aplicaciones para que su funcionalidad se pueda actualizar y reutilizar más fácilmente. Los archivos DLL también ayudan a reducir la sobrecarga de memoria cuando varias aplicaciones usan la misma funcionalidad al mismo tiempo, ya que aunque cada aplicación recibe su propia copia de los datos dll, las aplicaciones comparten el código DLL.

La Windows de programación de aplicaciones (API) se implementa como un conjunto de archivos DLL, por lo que cualquier proceso que use la API de Windows usa la vinculación dinámica.

-   [Acerca de Dynamic-Link bibliotecas](about-dynamic-link-libraries.md)
-   [Uso de Dynamic-Link bibliotecas](using-dynamic-link-libraries.md)
-   [Referencia de la biblioteca de vínculos dinámicos](dynamic-link-library-reference.md)

> [!Note]  
> Si es un usuario que experimenta dificultades con un archivo DLL en el equipo, debe ponerse en contacto con el servicio de soporte al cliente para el proveedor de software que publica el archivo DLL. Si cree que necesita soporte técnico para un producto de Microsoft (incluido Windows), vaya a nuestro sitio de soporte técnico en [support.microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ARCHIVOS DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
