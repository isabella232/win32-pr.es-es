---
description: Las funciones del cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red mediante la modificación de los cuadros de diálogo del sistema o la visualización de cuadros de diálogo personalizados.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific funciones del cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648615"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific funciones del cuadro de diálogo

Las funciones del cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red mediante la modificación de los cuadros de diálogo del sistema o la visualización de cuadros de diálogo personalizados.

Las siguientes funciones de cuadro de diálogo agregan botones al cuadro de diálogo **propiedades** del administrador de archivos. A continuación, el proveedor puede controlar los eventos de esos botones para realizar tareas específicas de la red. Tenga en cuenta que hay un límite en el número de botones que se pueden agregar. Por este motivo, los proveedores deben usar esta funcionalidad con moderación. Además, un proveedor puede no ser capaz de agregar un botón porque otros proveedores ya han utilizado el espacio disponible. Un proveedor de red debe controlar esta situación.



| Función                                           | Descripción                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Determina los nombres de los botones que se agregan a un cuadro de diálogo de propiedades para un recurso específico.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Se llama cuando un usuario hace clic en un botón agregado mediante la función [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Permite a los proveedores de red implementar su propia funcionalidad de búsqueda más allá de la que se proporciona en el cuadro de diálogo de **conexión** .<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Permite a los proveedores de red dar formato o modificar los nombres de red antes de que se presenten al usuario.<br/>                 |



 

 

 




