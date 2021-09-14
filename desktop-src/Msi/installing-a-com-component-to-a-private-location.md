---
description: Para forzar que una aplicación cliente COM use siempre la misma copia de un servidor COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor COM y el cliente.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Instalación de un componente COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072060"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Instalación de un componente COM en una ubicación privada

Para forzar que una aplicación cliente COM use siempre la misma copia de un servidor [](isolated-components.md) COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor COM y el cliente. Esto instala una copia privada del componente de servidor COM en una ubicación utilizada exclusivamente por la aplicación cliente. Haga lo siguiente al crear el paquete:

-   Coloque el archivo DLL del servidor COM y .exe cliente en componentes independientes.
-   Escriba un registro en la tabla [IsolatedComponent](isolatedcomponent-table.md) con el componente COM-client en la columna Component Shared (Componente compartido) y la aplicación cliente \_ en la columna Aplicación de \_ componentes. Incluya la [acción IsolateComponents en](isolatecomponents-action.md) las tablas de secuencia.
-   Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro de tabla [Component](component-table.md) para Component \_ Shared. El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



