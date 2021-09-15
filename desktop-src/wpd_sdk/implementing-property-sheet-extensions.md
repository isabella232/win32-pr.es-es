---
description: Implementar extensiones de hoja de propiedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementar extensiones de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571220"
---
# <a name="implementing-property-sheet-extensions"></a>Implementar extensiones de hoja de propiedades

La extensión de espacio de nombres WPD admite hojas de propiedades extensibles. Estos son los diálogos de propiedades que aparecen cuando un usuario hace clic con el botón derecho en un objeto, como un archivo o una carpeta, y selecciona **Propiedades.** Algunas aplicaciones WPD aprovecharán estas hojas de propiedades extensibles para mostrar las propiedades del contenido del lado del dispositivo (u objetos que residen en el dispositivo).

Las hojas de propiedades extensibles son compatibles con las interfaces descritas en la tabla siguiente. Para obtener más información sobre cualquiera de estas interfaces, consulte el SDK Windows.



| Interfaz           | Descripción                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Se usa para pasar la matriz PIDL del menú contextual al controlador de menú contextual.      |
| IPropertySetStorage | Esta interfaz se usa para recuperar las propiedades de WPD para el objeto especificado.      |
| IPropertyStorage    | Esta interfaz también se usa para recuperar las propiedades de WPD para el objeto especificado. |
| IShellExtInit       | Inicializa el Windows de Shell de Vista para el menú contextual.         |
| IShellPropSheetExt  | Admite la adición de extensiones de hoja de propiedades.                              |



 

Las hojas de propiedades para WPD se implementan como cualquier otra hoja de propiedades Windows Vista. Si ya ha implementado un controlador de hoja de propiedades, puede modificar el código existente para que admita contenido del lado del dispositivo. Si nunca ha creado un controlador de menú contextual, consulte el tema Creating Property Sheet Handlers (Creación de controladores de hoja de propiedades) en Windows SDK.

Los dos puntos en los que un controlador de hoja de propiedades de WPD difiere de cualquier otro controlador se encuentra en el registro del controlador y en la compatibilidad con el contenido del lado del dispositivo.

 

 



