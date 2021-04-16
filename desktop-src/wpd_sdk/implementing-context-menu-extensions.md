---
description: Implementar extensiones de menú contextual
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementar extensiones de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716065"
---
# <a name="implementing-context-menu-extensions"></a>Implementar extensiones de menú contextual

La extensión de espacio de nombres de WPD admite menús de contexto extensible (o acceso directo). Estos son los menús que aparecen cuando un usuario hace clic con el botón secundario en un objeto, como un archivo o una carpeta. Algunas aplicaciones de WPD aprovecharán estos menús extensibles para admitir operaciones en el contenido del dispositivo (o los objetos que residen en el dispositivo).

Los menús contextuales extensibles son compatibles con las interfaces descritas en la tabla siguiente. Para obtener más información sobre cualquiera de estas interfaces, vea el Windows SDK.



| Interfaz           | Descripción                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | El shell de Windows Vista llama a los métodos de esta interfaz para crear o combinar el nuevo menú contextual con el objeto dado. |
| IDataObject         | Se usa para pasar la matriz PIDL del menú contextual al controlador del menú contextual.                                                    |
| IPropertySetStorage | Esta interfaz se utiliza para recuperar las propiedades de WPD para el objeto especificado.                                                    |
| IPropertyStorage    | Esta interfaz también se utiliza para recuperar las propiedades de WPD para el objeto dado.                                               |
| IShellExtInit       | Inicializa las extensiones de Shell de Windows Vista para el menú contextual.                                                       |
| IStream             | Que se va a proporcionar.                                                                                                            |



 

Los menús contextuales de WPD se implementan como cualquier otro menú contextual en Windows Vista. Si ya ha implementado un controlador de menú contextual, puede modificar el código existente para que sea compatible con el contenido del dispositivo. Si nunca ha creado un controlador de menú contextual, consulte el tema creación de controladores de menú contextual en el Windows SDK.

Los dos puntos en los que un controlador de menú contextual de WPD difiere de cualquier otro controlador se encuentran en el registro del controlador y en la compatibilidad del contenido del dispositivo.

 

 



