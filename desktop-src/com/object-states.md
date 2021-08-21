---
title: Estados de objeto
description: Estados de objeto
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66cbae9ca9d350c4d8436f99cf2934aa8ab653dc30f4d9196f9d007c61b490a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105143"
---
# <a name="object-states"></a>Estados de objeto

Un objeto compuesto existe en uno de estos tres estados: pasivo, cargado o en ejecución. El estado de un objeto de documento compuesto describe la relación entre el objeto en su contenedor y la aplicación responsable de su creación. En la tabla siguiente se resumen estos estados.



| Estado de objeto       | Descripción                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pasivo<br/> | El objeto de documento compuesto solo existe en el almacenamiento, ya sea en el disco o en una base de datos. En este estado, el objeto no está disponible para su visualización o edición.<br/>                                                                                                                                                                                                                                   |
| Cargado<br/>  | Las estructuras de datos del objeto creadas por el controlador de objetos están en la memoria del contenedor. El contenedor ha establecido la comunicación con el controlador de objetos y hay datos de presentación almacenados en caché disponibles para representar el objeto. El controlador de objetos procesa las llamadas. Este estado, debido a su baja sobrecarga, se usa cuando un usuario simplemente ve o imprime un objeto.<br/> |
| En ejecución<br/> | Se han creado los objetos que controlan la comunicación remota y se está ejecutando la aplicación de servidor OLE. Las interfaces del objeto son accesibles y el contenedor puede recibir notificaciones de cambios. En este estado, un usuario final puede editar o manipular el objeto.<br/>                                                                                                                    |



 

Para obtener más información, vea los temas siguientes:

-   [Especificación del estado cargado](entering-the-loaded-state.md)
-   [Especificar el estado en ejecución](entering-the-running-state.md)
-   [Especificación del estado pasivo](entering-the-passive-state.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 





