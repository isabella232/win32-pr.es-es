---
description: En algunos casos, los autores pueden decidir que deben romper las reglas para crear componentes, como se describe en organización de aplicaciones en componentes y modificación del código de componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: ¿Qué ocurre si se interrumpen las reglas de componentes?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f61a0a819856c5014aa70acfaeb46be5043e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678067"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>¿Qué ocurre si se interrumpen las reglas de componentes?

En algunos casos, los autores pueden decidir que deben romper las reglas para crear componentes, como se describe en [organización de aplicaciones en componentes](organizing-applications-into-components.md) y [modificación del código de componente](changing-the-component-code.md). Los autores deben tener en cuenta las posibles consecuencias de hacerlo y, de lo contrario, garantizar que sus componentes nunca se instalen donde puedan dañar otras aplicaciones o componentes del sistema del usuario.

En la lista siguiente se describen las formas en las que los autores pueden interrumpir las reglas de componentes recomendadas y las posibles consecuencias.

Un autor agrega recursos a un componente sin cambiar el código del componente.

-   Los productos instalados con el componente anterior no tienen información sobre los recursos agregados en su base de datos de instalación.
-   Si un nuevo producto que tiene los recursos agregados y un producto anterior se instalan en el mismo equipo, los recursos se pueden dejar atrás si primero se desinstala el nuevo producto.
-   Un producto anterior sin los recursos agregados no puede reparar la versión más reciente del componente. Al volver a instalar el producto anterior, no se restauran los recursos agregados.

Un autor quita los recursos de un componente sin cambiar el código del componente.

-   Los productos instalados con el nuevo componente no tienen información sobre los recursos que se han quitado en la base de datos de instalación.
-   Si un producto antiguo, con la información de recursos y un nuevo producto se instalan en el mismo equipo, los recursos se pueden dejar atrás si primero se desinstala el producto anterior.
-   Un nuevo producto con los recursos quitados no puede reparar la versión anterior del producto. Al volver a instalar el nuevo producto, no se restauran los recursos que se han quitado.

Un autor incluye un archivo que no es compatible con versiones anteriores sin cambiar el código del componente.

Si un archivo incompatible está incluido en un componente sin cambiar el código de componente, el [control de versiones de archivo predeterminado](default-file-versioning.md) hace que el instalador sobrescriba el archivo original con el archivo incompatible más reciente. Esto puede dañar los productos antiguos que necesiten el archivo original. También puede impedir que el instalador repare el producto antiguo porque la versión del archivo de ruta de acceso de la clave de un componente determina la versión del componente. Si ya hay instalada una versión más reciente del archivo de ruta de acceso de la clave, el instalador no instala una versión anterior del componente. Para obtener más información, vea [reglas de control de versiones de archivos](file-versioning-rules.md). En este caso, se debe quitar el nuevo producto antes de que se pueda volver a instalar el producto anterior.

-   El [control de versiones de archivo predeterminado](default-file-versioning.md) hace que el instalador sobrescriba el archivo original con el archivo incompatible más reciente.
-   Los productos antiguos que necesitan el archivo original están dañados.
-   También puede impedir que el instalador repare el producto antiguo porque la versión del archivo de ruta de acceso de la clave de un componente determina la versión del componente. Si ya hay instalada una versión más reciente del archivo de ruta de acceso de la clave, el instalador no instala la versión anterior del componente. Para obtener más información, vea [reglas de control de versiones de archivos](file-versioning-rules.md). En este caso, se debe quitar el nuevo producto antes de que se pueda volver a instalar el producto anterior.

Un autor incluye el mismo recurso en dos componentes diferentes.

Si dos componentes tienen un recurso con el mismo nombre y la misma ubicación y ambos componentes se instalan en la misma carpeta, la eliminación de ambos componentes quita el recurso común, lo que daña el componente restante.

-   Al desinstalar cualquiera de los componentes, se quita el recurso y se rompe el otro componente.
-   El mecanismo de recuento de referencias de componentes está dañado.

 

 



