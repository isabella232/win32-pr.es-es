---
description: Un componente es una parte de la aplicación o el producto que se va a instalar.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Componentes del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 449a54a2e0c60eb3385b7ac1d606c2517337bf664f96c5df88517a8097cdcaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995521"
---
# <a name="windows-installer-components"></a>Windows Componentes del instalador

Un componente es una parte de la aplicación o el producto que se va a instalar. Algunos ejemplos de componentes son archivos únicos, un grupo de archivos relacionados, objetos COM, registro, claves del Registro, accesos directos, recursos, bibliotecas agrupadas en un directorio o fragmentos de código compartidos como MFC o DAO.

El servicio de instalador instala o quita un componente como una sola pieza coherente. Realiza un seguimiento de cada componente por el GUID del identificador de componente correspondiente especificado en la columna ComponentId de la [tabla Component](component-table.md).

> [!Note]  
> Dos componentes que comparten el mismo identificador de componente se tratan como varias instancias del mismo componente independientemente de su contenido real. Solo se instala una única instancia de cualquier componente en el equipo de un usuario. Por lo tanto, varias características o aplicaciones pueden compartir algunos componentes.

 

Dado que los componentes se comparten normalmente, el autor de un paquete de instalación debe seguir reglas estrictas al especificar los componentes de una característica o aplicación. Esto es esencial para el funcionamiento correcto del Windows de recuento de referencias del instalador. Para obtener más información, [vea Organización de aplicaciones en componentes](organizing-applications-into-components.md).

En resumen, estas reglas son:

-   Cada componente debe almacenarse en una sola carpeta.
-   Nunca se debe enviar ningún archivo, entrada del Registro, acceso directo u otros recursos como miembro de más de un componente. Esto se aplica a todos los productos, versiones de productos y empresas.

Para obtener más información sobre el uso de componentes, vea

-   [Instalación de un componente que falta](installing-a-missing-component.md)
-   [Instalación de componentes permanentes, archivos, fuentes y claves del Registro](installing-permanent-components-files-fonts-registry-keys.md)
-   [Uso de componentes calificados](using-qualified-components.md)
-   [Uso de componentes transitivos](using-transitive-components.md)
-   [Trabajar con características y componentes](working-with-features-and-components.md)
-   [Creación de un paquete grande](authoring-a-large-package.md)
-   [Comprobar la instalación de características, componentes, archivos](checking-the-installation-of-features-components-files.md)
-   [Buscar una característica o un componente rotos](searching-for-a-broken-feature-or-component.md)
-   [Publicar productos, características y componentes](publishing-products-features-and-components.md)

 

 



