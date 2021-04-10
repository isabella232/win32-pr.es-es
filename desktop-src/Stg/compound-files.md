---
title: archivos compuestos
description: Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada archivos compuestos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268390"
---
# <a name="compound-files"></a>archivos compuestos

Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada archivos compuestos. El uso de archivos compuestos le permite guardar el trabajo de codificación de su propia implementación de almacenamiento estructurado y confiere varias ventajas adicionales derivadas de la adhesión a un estándar definido. Entre estos beneficios, se incluyen los siguientes:

-   **Independencia del sistema de archivos y la plataforma**. Dado que la implementación de archivos compuestos de COM se ejecuta sobre sistemas de archivos sin formato existentes, las aplicaciones pueden abrir los archivos compuestos almacenados en el sistema de archivos FAT, en el sistema de archivos NTFS o en los sistemas de archivos de Macintosh con cualquiera de los demás sistemas de archivos.
-   **Búsqueda**. Dado que los objetos independientes de un archivo compuesto se guardan en un formato estándar y se puede tener acceso a ellos mediante interfaces y API COM estándar, cualquier utilidad del explorador que use estas interfaces y API puede enumerar los objetos del archivo, aunque los datos de un objeto determinado pueden estar en un formato de propiedad.
-   **Acceso a determinados datos internos**. Dado que la implementación de archivos compuestos proporciona formas estándar de escribir determinados tipos de datos (información de Resumen, por ejemplo), las aplicaciones pueden leer estos datos mediante interfaces y API COM.

 

 




