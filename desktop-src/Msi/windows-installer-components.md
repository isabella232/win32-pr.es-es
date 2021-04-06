---
description: Un componente es una parte de la aplicación o del producto que se va a instalar.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componentes de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002245"
---
# <a name="windows-installer-components"></a>Componentes de Windows Installer

Un componente es una parte de la aplicación o del producto que se va a instalar. Entre los ejemplos de componentes se incluyen archivos únicos, un grupo de archivos relacionados, objetos COM, registro, claves del registro, accesos directos, recursos, bibliotecas agrupadas en un directorio o fragmentos de código compartidos, como MFC o DAO.

El servicio del instalador instala o quita un componente como una única pieza coherente. Realiza un seguimiento de todos los componentes por el GUID del identificador de componente correspondiente especificado en la columna ComponentId de la [tabla de componentes](component-table.md).

> [!Note]  
> Dos componentes que comparten el mismo identificador de componente se tratan como varias instancias del mismo componente, independientemente de su contenido real. Solo se instala una única instancia de cualquier componente en el equipo de un usuario. Por lo tanto, varias características o aplicaciones pueden compartir algunos componentes.

 

Dado que los componentes suelen compartirse, el autor de un paquete de instalación debe seguir reglas estrictas al especificar los componentes de una característica o aplicación. Esto es esencial para el funcionamiento correcto del mecanismo de recuento de referencias de Windows Installer. Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).

En Resumen, estas reglas son:

-   Cada componente debe almacenarse en una sola carpeta.
-   Ningún archivo, entrada del registro, acceso directo u otros recursos deben enviarse como miembro de más de un componente. Esto se aplica a los productos, versiones de producto y compañías.

Para obtener más información acerca del uso de los componentes de, vea.

-   [Instalación de un componente que falta](installing-a-missing-component.md)
-   [Instalación de componentes permanentes, archivos, fuentes y claves del registro](installing-permanent-components-files-fonts-registry-keys.md)
-   [Uso de componentes calificados](using-qualified-components.md)
-   [Uso de componentes transitivos](using-transitive-components.md)
-   [Trabajar con características y componentes](working-with-features-and-components.md)
-   [Crear un paquete grande](authoring-a-large-package.md)
-   [Comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md)
-   [Buscar una característica o componente interrumpido](searching-for-a-broken-feature-or-component.md)
-   [Publicar productos, características y componentes](publishing-products-features-and-components.md)

 

 



