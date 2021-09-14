---
description: Un administrador puede forzar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM en un paquete existente&8212; sin afectar a otras aplicaciones \#&8212; especificando una relación de componentes aislados entre el servidor \# COM y el cliente.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Hacer que un componente COM en un paquete existente sea privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071924"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Hacer que un componente COM en un paquete existente sea privado

Un administrador puede forzar a una aplicación cliente COM a usar siempre la misma copia de un servidor [](isolated-components.md) COM en un paquete existente, sin afectar a otras aplicaciones, especificando una relación de componentes aislados entre el servidor COM y el cliente. Esto instala una copia privada del componente de servidor COM en una ubicación utilizada exclusivamente por la aplicación cliente. El administrador debe usar transformaciones o una herramienta de creación de paquetes para hacer lo siguiente:

-   Coloque el archivo DLL del servidor COM y .exe cliente en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente COM-client en la columna Component Shared (Componente compartido) y la aplicación cliente \_ en la columna Component Application \_ (Aplicación de componentes). Incluya la [acción IsolateComponents en](isolatecomponents-action.md) las tablas de secuencia.
-   Establezca el **bit msidbComponentAttributesSharedDllRefCount** en el registro [de tabla Component](component-table.md) para Component \_ Shared. El instalador requiere este recuento de referencias global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



