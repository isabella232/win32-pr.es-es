---
description: Las funciones de cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red modificando los cuadros de diálogo del sistema o mostrando cuadros de diálogo personalizados.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific funciones del cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374983"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific funciones del cuadro de diálogo

Las funciones de cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red modificando los cuadros de diálogo del sistema o mostrando cuadros de diálogo personalizados.

Las siguientes funciones de cuadro de diálogo agregan botones al cuadro de diálogo Propiedades **del** Administrador de archivos . A continuación, el proveedor puede controlar los eventos de esos botones para realizar tareas específicas de la red. Tenga en cuenta que hay un límite en el número de botones que se pueden agregar. Por este problema, los proveedores deben usar esta funcionalidad con moderación. Además, es posible que un proveedor no pueda agregar un botón porque otros proveedores ya han usado el espacio disponible. Un proveedor de red debe controlar esta situación.



| Función                                           | Descripción                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Determina los nombres de los botones agregados a un cuadro de diálogo de propiedad para un recurso específico.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Se llama cuando un usuario hace clic en un botón agregado mediante la [**función NPGetPropertyText.**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Permite a los proveedores de red implementar su propia funcionalidad de búsqueda más allá de la proporcionada en el **cuadro de diálogo** Conexión.<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Permite a los proveedores de red dar formato o modificar los nombres de red antes de que se presenten al usuario.<br/>                 |



 

 

 




