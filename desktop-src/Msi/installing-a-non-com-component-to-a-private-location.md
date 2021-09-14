---
description: Para forzar que una aplicación cliente use siempre la misma copia de un servidor que no es COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor y el cliente.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Instalación de un componente que no es COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072059"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Instalación de un componente que no es COM en una ubicación privada

Para forzar que una aplicación cliente use siempre la misma copia de un servidor [](isolated-components.md) que no es COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor y el cliente. Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente. Haga lo siguiente al crear el paquete:

-   Coloque el archivo DLL del servidor y .exe cliente en componentes independientes.
-   Escriba un registro en la [tabla IsolatedComponent con](isolatedcomponent-table.md) el componente de cliente en la columna Componente compartido y la aplicación cliente \_ en la columna Aplicación de componentes \_ . Incluya la [acción IsolateComponents en](isolatecomponents-action.md) las tablas de secuencia.
-   Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro [de tabla Component](component-table.md) para Component \_ Shared. El instalador requiere este recuento de referencias global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.
-   Evite crear una ruta de acceso registrada compartida entre componentes.

 

 



