---
title: archivos compuestos
description: Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada Archivos compuestos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 302f7587817f07ec18900f537189a2571c883b0fc43a58eddb823a40fe1c0db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867465"
---
# <a name="compound-files"></a>archivos compuestos

Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada Archivos compuestos. El uso de archivos compuestos le ahorra el trabajo de codificar su propia implementación de almacenamiento estructurado y le confiere varias ventajas adicionales derivadas de la adhesión a un estándar definido. Entre estos beneficios, se incluyen los siguientes:

-   **Independencia del sistema de archivos y de la plataforma**. Dado que la implementación de archivos compuestos de COM se ejecuta sobre sistemas de archivos planos existentes, las aplicaciones pueden abrir los archivos compuestos almacenados en el sistema de archivos FAT, el sistema de archivos NTFS o los sistemas de archivos Macintosh mediante cualquiera de los demás sistemas de archivos.
-   **Que permite búsquedas.** Dado que los objetos independientes de un archivo compuesto se guardan en un formato estándar y se puede acceder a ellos mediante interfaces COM y API estándar, cualquier utilidad de explorador que use estas interfaces y API puede enumerar los objetos del archivo, aunque los datos de un objeto determinado puedan estar en un formato propietario.
-   **Acceso a determinados datos internos.** Dado que la implementación de archivos compuestos proporciona formas estándar de escribir determinados tipos de datos (por ejemplo, información de resumen), las aplicaciones pueden leer estos datos mediante interfaces COM y API.

 

 




