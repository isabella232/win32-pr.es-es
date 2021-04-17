---
description: Un administrador puede obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM en un paquete existente&\# 8212; sin que afecte a otras aplicaciones&\# 8212; especificando una relación de componentes aislados entre el servidor y el cliente.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Convertir un componente que no sea COM en un paquete existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677466"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Convertir un componente que no sea COM en un paquete existente privado

Un administrador puede obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM en un paquete existente, sin que afecte a otras aplicaciones, mediante la especificación de una relación de [componentes aislados](isolated-components.md) entre el servidor y el cliente. Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente. El administrador debe usar transformaciones o una herramienta de creación de paquetes para realizar lo siguiente:

-   Coloque el archivo DLL del servidor y el cliente. exe en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes. Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.
-   Establezca el bit **msidbComponentAttributesSharedDllRefCount** en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared. El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.

 

 



