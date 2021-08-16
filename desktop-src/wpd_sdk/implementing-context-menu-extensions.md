---
description: Implementar extensiones de menú contextual
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementar extensiones de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090f37b4cf77f9508e8c149ef6389297c561e1a4e574ef767f3a5e5c7e07fe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194688"
---
# <a name="implementing-context-menu-extensions"></a>Implementar extensiones de menú contextual

La extensión de espacio de nombres WPD admite menús contextuales extensibles (o accesos directos). Estos son los menús que aparecen cuando un usuario hace clic con el botón derecho en un objeto, como un archivo o una carpeta. Algunas aplicaciones WPD aprovecharán estos menús extensibles para admitir operaciones en el contenido del lado del dispositivo (u objetos que residen en el dispositivo).

Los menús contextuales extensibles son compatibles con las interfaces descritas en la tabla siguiente. Para obtener más información sobre cualquiera de estas interfaces, consulte el SDK Windows.



| Interfaz           | Descripción                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | El Windows Shell de Vista llama a los métodos de esta interfaz para crear o combinar el nuevo menú contextual con el objeto especificado. |
| IDataObject         | Se usa para pasar la matriz PIDL del menú contextual al controlador de menú contextual.                                                    |
| IPropertySetStorage | Esta interfaz se usa para recuperar las propiedades de WPD para el objeto especificado.                                                    |
| IPropertyStorage    | Esta interfaz también se usa para recuperar las propiedades de WPD para el objeto especificado.                                               |
| IShellExtInit       | Inicializa el Windows de Shell de Vista para el menú contextual.                                                       |
| Istream             | Que se va a proporcionar.                                                                                                            |



 

Los menús contextuales de WPD se implementan como cualquier otro menú contextual en Windows Vista. Si ya ha implementado un controlador de menú contextual, puede modificar el código existente para que admita contenido del lado del dispositivo. Si nunca ha creado un controlador de menú contextual, vea el tema Creating Context Menu Handlers (Creación de controladores de menú contextual) en el SDK Windows.

Los dos puntos en los que un controlador de menú contextual de WPD difiere de cualquier otro controlador está en el registro del controlador y en la compatibilidad con el contenido del lado del dispositivo.

 

 



