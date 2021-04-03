---
description: Para obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el cliente y el servidor COM.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Instalar un componente COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908307"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Instalar un componente COM en una ubicación privada

Para obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM, cree el paquete de instalación de la aplicación para especificar una relación de [componentes aislados](isolated-components.md) entre el cliente y el servidor com. De este modo se instala una copia privada del componente COM-Server en una ubicación utilizada exclusivamente por la aplicación cliente. Al crear el paquete, realice lo siguiente:

-   Coloque el archivo DLL del servidor COM y el cliente. exe en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente com en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes. Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.
-   Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared. El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



