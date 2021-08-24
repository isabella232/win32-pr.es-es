---
description: Implementar extensiones de hoja de propiedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementar extensiones de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b4f74559176ecc0c411f75e7ca630db152a51109f09ecdca47a62d0113e70c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590285"
---
# <a name="implementing-property-sheet-extensions"></a>Implementar extensiones de hoja de propiedades

La extensión de espacio de nombres WPD admite hojas de propiedades extensibles. Estos son los diálogos de propiedades que aparecen cuando un usuario hace clic con el botón derecho en un objeto, como un archivo o una carpeta, y selecciona **Propiedades.** Algunas aplicaciones WPD aprovecharán estas hojas de propiedades extensibles para mostrar las propiedades del contenido del lado del dispositivo (u objetos que residen en el dispositivo).

Las hojas de propiedades extensibles son compatibles con las interfaces descritas en la tabla siguiente. Para obtener más información sobre cualquiera de estas interfaces, consulte el SDK Windows.



| Interfaz           | Descripción                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Se usa para pasar la matriz PIDL del menú contextual al controlador de menú contextual.      |
| IPropertySetStorage | Esta interfaz se usa para recuperar las propiedades de WPD para el objeto especificado.      |
| IPropertyStorage    | Esta interfaz también se usa para recuperar las propiedades de WPD para el objeto especificado. |
| IShellExtInit       | Inicializa las extensiones Windows Shell de Vista para el menú contextual.         |
| IShellPropSheetExt  | Admite la adición de extensiones de hoja de propiedades.                              |



 

Las hojas de propiedades para WPD se implementan como cualquier otra hoja de propiedades en Windows Vista. Si ya ha implementado un controlador de hoja de propiedades, puede modificar el código existente para que admita contenido del lado del dispositivo. Si nunca ha creado un controlador de menú contextual, consulte el tema Creating Property Sheet Handlers (Creación de controladores de hoja de propiedades) en Windows SDK.

Los dos puntos en los que un controlador de hoja de propiedades de WPD difiere de cualquier otro controlador se encuentra en el registro del controlador y en la compatibilidad con el contenido del lado del dispositivo.

 

 



