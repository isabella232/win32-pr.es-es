---
description: Los contadores de rendimiento específicos de la aplicación pueden ayudarle a optimizar el rendimiento mientras desarrolla y depura la aplicación.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Agregar contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaf66d6a0e2f0c98ad0e9fe3cc66069509d4c2391ab74e4ecaa17d6780f4561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034005"
---
# <a name="adding-performance-counters"></a>Agregar contadores de rendimiento

> [!IMPORTANT]
> Debido a limitaciones significativas de rendimiento y confiabilidad, el método para proporcionar datos de contadores de rendimiento que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en Proporcionar datos de contador mediante la versión [2.0 para](providing-counter-data-using-version-2-0.md) crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar también ese método.

Los contadores de rendimiento específicos de la aplicación pueden ayudarle a optimizar el rendimiento mientras desarrolla y depura la aplicación. Una vez completada e instalada la aplicación en los sistemas de destino, los contadores pueden ayudar a los administradores del sistema a ajustar la configuración configurable de la aplicación.

## <a name="adding-a-performance-object-and-its-counters"></a>Agregar un objeto de rendimiento y sus contadores

1. Diseñe los tipos de objeto y los contadores de la aplicación. Para obtener más información, vea [Diseño de objetos y contadores.](object-and-counter-design.md)
2. Cree un archivo de inicialización (.ini) que contenga los nombres y descripciones de los objetos de rendimiento y los contadores que proporcione. Para obtener más información, [vea Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).
3. Cree un archivo de encabezado (.h) que contenga los desplazamientos relativos en los que se instalarán los contadores y los objetos de contador en el Registro. Para obtener más información, [vea Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configure las entradas de supervisión de rendimiento necesarias en el Registro. Esto incluye los pasos siguientes.
    1. Cree una clave del Registro en la **clave Servicios** de la aplicación. Si no tiene este tipo de nodo, cándalo con la siguiente clave del Registro: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Para más información, consulte [Creación de la clave de rendimiento de la aplicación.](creating-the-applications-performance-key.md)
    2. Use la **utilidad lodctr** con los archivos .ini y .h para instalar la información en el Registro. Esta utilidad solo se realiza correctamente si existe una clave de rendimiento en la **clave Servicios** de la aplicación. Para obtener más información, [vea Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).
5. Cree un archivo DLL de rendimiento que contenga un conjunto de funciones exportadas que proporcionen los datos del contador consultadas al consumidor. Para obtener más información, vea [Crear un archivo DLL de extensión de rendimiento.](creating-a-performance-extension-dll.md)
6. Modifique el archivo de instalación de la aplicación para automatizar la adición de información al Registro (como se describe en el paso 4) y copie el archivo DLL de rendimiento en el directorio de la aplicación durante la instalación.

Para obtener información sobre otras entradas del Registro, vea [Crear otras entradas del Registro.](creating-other-registry-entries.md)
