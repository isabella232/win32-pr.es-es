---
description: En algunos casos, los autores pueden decidir que necesitan interrumpir las reglas para crear componentes, como se describe en Organización de aplicaciones en componentes y Cambio del código de componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: ¿Qué ocurre si se han roto las reglas de componentes?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f830fa402da44be992d74adc957d88a19442dcbb51173a87e79fa2266552a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498775"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>¿Qué ocurre si se han roto las reglas de componentes?

En algunos casos, los autores pueden decidir que necesitan interrumpir las reglas para crear componentes, como se describe en [Organización](organizing-applications-into-components.md) de aplicaciones en componentes y Cambio [del código de componente](changing-the-component-code.md). Los autores deben ser conscientes de las posibles consecuencias de hacerlo y, de lo contrario, deben garantizar que sus componentes nunca se instalen donde puedan dañar otras aplicaciones o componentes del sistema del usuario.

En la lista siguiente se describen las formas en que los autores a veces inscriben las reglas de componentes recomendadas y las posibles consecuencias.

Un autor agrega recursos a un componente sin cambiar el código del componente.

-   Los productos instalados con el componente anterior no tienen información sobre los recursos agregados en su base de datos de instalación.
-   Si un nuevo producto que tiene los recursos agregados y un producto antiguo están instalados en el mismo equipo, los recursos se pueden dejar atrás si el nuevo producto se desinstala primero.
-   Un producto antiguo sin los recursos agregados no puede reparar la versión más reciente del componente. La reinstalación del producto anterior no restaura los recursos agregados.

Un autor quita recursos de un componente sin cambiar el código del componente.

-   Los productos instalados con el nuevo componente no tienen información sobre los recursos quitados en su base de datos de instalación.
-   Si tanto un producto antiguo, con la información de recursos como un nuevo producto están instalados en el mismo equipo, los recursos se pueden dejar atrás si primero se desinstala el producto antiguo.
-   Un nuevo producto con los recursos quitados no puede reparar la versión anterior del producto. La reinstalación del nuevo producto no restaura los recursos quitados.

Un autor incluye un archivo que no es compatible con versiones anteriores sin cambiar el código del componente.

Si se incluye un archivo incompatible en un componente sin cambiar el código del [componente,](default-file-versioning.md) el control de versiones de archivo predeterminado hace que el instalador sobrescriba el archivo original con el archivo incompatible más reciente. Esto puede dañar los productos antiguos que necesitan el archivo original. También puede impedir que el instalador repare el producto antiguo porque la versión del archivo de ruta de acceso de clave de un componente determina la versión del componente. Si ya está instalada una versión más reciente del archivo de ruta de acceso de clave, el instalador no instala una versión anterior del componente. Para obtener más información, vea [Reglas de control de versiones de archivos](file-versioning-rules.md). En este caso, el nuevo producto debe quitarse antes de que se pueda volver a instalar el producto anterior.

-   [El control de versiones de archivo](default-file-versioning.md) predeterminado hace que el instalador sobrescriba el archivo original con el archivo incompatible más reciente.
-   Los productos antiguos que necesitan el archivo original están dañados.
-   También puede impedir que el instalador repare el producto antiguo porque la versión del archivo de ruta de acceso de clave de un componente determina la versión del componente. Si ya está instalada una versión más reciente del archivo de ruta de acceso de clave, el instalador no instala la versión anterior del componente. Para obtener más información, vea [Reglas de control de versiones de archivos](file-versioning-rules.md). En este caso, el nuevo producto debe quitarse antes de que se pueda volver a instalar el producto anterior.

Un autor incluye el mismo recurso en dos componentes diferentes.

Si dos componentes tienen un recurso con el mismo nombre y ubicación y ambos componentes están instalados en la misma carpeta, la eliminación de cualquiera de los componentes quita el recurso común, lo que daña el componente restante.

-   Al desinstalar cualquiera de los componentes se quita el recurso y se interrumpe el otro componente.
-   El mecanismo de recuento de referencias de componentes está dañado.

 

 



