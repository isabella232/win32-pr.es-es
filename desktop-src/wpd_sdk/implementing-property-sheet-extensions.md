---
description: Implementar extensiones de hoja de propiedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementar extensiones de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717145"
---
# <a name="implementing-property-sheet-extensions"></a>Implementar extensiones de hoja de propiedades

La extensión de espacio de nombres de WPD admite hojas de propiedades extensibles. Estos son los cuadros de diálogo de propiedades que aparecen cuando un usuario hace clic con el botón secundario en un objeto, como un archivo o una carpeta, y selecciona **propiedades**. Algunas aplicaciones de WPD aprovecharán estas hojas de propiedades extensibles para mostrar las propiedades del contenido del dispositivo (o los objetos que residen en el dispositivo).

Las interfaces que se describen en la tabla siguiente admiten hojas de propiedades extensibles. Para obtener más información sobre cualquiera de estas interfaces, vea el Windows SDK.



| Interfaz           | Descripción                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Se usa para pasar la matriz PIDL del menú contextual al controlador del menú contextual.      |
| IPropertySetStorage | Esta interfaz se utiliza para recuperar las propiedades de WPD para el objeto especificado.      |
| IPropertyStorage    | Esta interfaz también se utiliza para recuperar las propiedades de WPD para el objeto dado. |
| IShellExtInit       | Inicializa las extensiones de Shell de Windows Vista para el menú contextual.         |
| IShellPropSheetExt  | Admite la adición de extensiones de la hoja de propiedades.                              |



 

Las hojas de propiedades de WPD se implementan como cualquier otra hoja de propiedades de Windows Vista. Si ya ha implementado un controlador de la hoja de propiedades, puede modificar el código existente para que sea compatible con el contenido del dispositivo. Si nunca ha creado un controlador de menú contextual, consulte el tema crear controladores de hoja de propiedades en el Windows SDK.

Los dos puntos en los que un controlador de la hoja de propiedades de WPD difiere de cualquier otro controlador se encuentran en el registro del controlador y en la compatibilidad del contenido del dispositivo.

 

 



