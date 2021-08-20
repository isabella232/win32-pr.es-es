---
description: Un administrador puede forzar a una aplicación cliente a usar siempre la misma copia de un servidor que no es COM en un paquete existente&8212; sin afectar a otras aplicaciones \#&8212; especificando una relación de componentes aislados entre el servidor \# y el cliente.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Hacer que un componente que no sea COM en un paquete existente sea privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d89ca6e921213bb462d1b858154419bef416ffa263b8b63ca6d98660fe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945621"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Hacer que un componente que no sea COM en un paquete existente sea privado

Un administrador puede forzar a una aplicación cliente a usar siempre la misma copia de un servidor [](isolated-components.md) no COM en un paquete existente, sin afectar a otras aplicaciones, especificando una relación de componentes aislados entre el servidor y el cliente. Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente. El administrador debe usar transformaciones o una herramienta de creación de paquetes para hacer lo siguiente:

-   Coloque el archivo DLL del servidor y .exe cliente en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent con](isolatedcomponent-table.md) el componente de cliente en la columna Componente compartido y la aplicación cliente \_ en la columna Aplicación de componentes \_ . Incluya la [acción IsolateComponents en](isolatecomponents-action.md) las tablas de secuencia.
-   Establezca el **bit msidbComponentAttributesSharedDllRefCount** en el registro [de la tabla Component](component-table.md) para Component \_ Shared. El instalador requiere este recuento de referencias global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



