---
description: Para obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor y el cliente.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Instalar un componente que no es COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913497"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Instalar un componente que no es COM en una ubicación privada

Para obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM, cree el paquete de instalación de la aplicación para especificar una relación de [componentes aislados](isolated-components.md) entre el servidor y el cliente. Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente. Al crear el paquete, realice lo siguiente:

-   Coloque el archivo DLL del servidor y el cliente. exe en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes. Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.
-   Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared. El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.
-   Evite la creación de una ruta de acceso registrada compartida entre los componentes.

 

 



