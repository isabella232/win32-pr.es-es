---
description: Un administrador puede obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM en un paquete existente&\# 8212; sin afectar a otras aplicaciones&\# 8212; especificando una relación de componentes aislados entre el servidor com y el cliente.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Convertir un componente COM en un paquete existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678253"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Convertir un componente COM en un paquete existente privado

Un administrador puede obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM en un paquete existente, sin que afecte a otras aplicaciones, mediante la especificación de una relación de [componentes aislados](isolated-components.md) entre el cliente y el servidor com. De este modo se instala una copia privada del componente COM-Server en una ubicación utilizada exclusivamente por la aplicación cliente. El administrador debe usar transformaciones o una herramienta de creación de paquetes para realizar lo siguiente:

-   Coloque el archivo DLL del servidor COM y el cliente. exe en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente com en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes. Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.
-   Establezca el bit **msidbComponentAttributesSharedDllRefCount** en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared. El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



