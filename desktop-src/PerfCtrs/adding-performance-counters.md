---
description: Los contadores de rendimiento específicos de la aplicación pueden ayudarle a ajustar el rendimiento mientras desarrolla y depura la aplicación.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Agregar contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8660af9406de4dedec3ecbd76169a23b342aa7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667349"
---
# <a name="adding-performance-counters"></a>Agregar contadores de rendimiento

> [!IMPORTANT]
> Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método también.

Los contadores de rendimiento específicos de la aplicación pueden ayudarle a ajustar el rendimiento mientras desarrolla y depura la aplicación. Una vez que la aplicación se haya completado e instalado en los sistemas de destino, los contadores pueden ayudar a los administradores del sistema a ajustar la configuración de la aplicación.

## <a name="adding-a-performance-object-and-its-counters"></a>Agregar un objeto de rendimiento y sus contadores

1. Diseñe los tipos de objeto y los contadores de la aplicación. Para obtener más información, vea [diseño de objetos y contadores](object-and-counter-design.md).
2. Cree un archivo de inicialización (. ini) que contenga los nombres y descripciones de los objetos y contadores de rendimiento que proporcione. Para obtener más información, vea [Agregar nombres y descripciones de contadores al registro](adding-counter-names-and-descriptions-to-the-registry.md).
3. Cree un archivo de encabezado (. h) que contenga los desplazamientos relativos en los que se instalarán los objetos de contador y los contadores en el registro. Para obtener más información, vea [Agregar nombres y descripciones de contadores al registro](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configure las entradas de supervisión de rendimiento necesarias en el registro. Esto incluye los pasos siguientes.
    1. Cree una clave del registro en la clave de **servicios** de la aplicación. Si no tiene este tipo de nodo, créelo en la siguiente clave del registro: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Para obtener más información, consulte [crear la clave de rendimiento de la aplicación](creating-the-applications-performance-key.md).
    2. Use la utilidad **LODCTR** con los archivos. ini y. h para instalar la información en el registro. Esta utilidad solo se realiza correctamente si existe una clave de rendimiento en la clave de **servicios** de la aplicación. Para obtener más información, vea [Agregar nombres y descripciones de contadores al registro](adding-counter-names-and-descriptions-to-the-registry.md).
5. Cree un archivo DLL de rendimiento que contenga un conjunto de funciones exportadas que proporcionen los datos del contador consultado al consumidor. Para obtener más información, consulte [crear un archivo dll de extensión de rendimiento](creating-a-performance-extension-dll.md).
6. Modifique el archivo de instalación de la aplicación para automatizar la adición de información al registro (como se describe en el paso 4) y copie el archivo DLL de rendimiento en el directorio de la aplicación en el programa de instalación.

Para obtener información acerca de las entradas del registro adicionales, vea [crear otras entradas del registro](creating-other-registry-entries.md).
