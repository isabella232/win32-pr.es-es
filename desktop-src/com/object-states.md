---
title: Estados de objeto
description: Estados de objeto
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704585"
---
# <a name="object-states"></a>Estados de objeto

Un objeto compuesto existe en uno de tres Estados: pasivo, cargado o en ejecución. El estado de un objeto de documento compuesto describe la relación entre el objeto en su contenedor y la aplicación responsable de su creación. En la tabla siguiente se resumen estos Estados.



| Estado de objeto       | Descripción                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pasivo<br/> | El objeto de documento compuesto solo existe en el almacenamiento, ya sea en el disco o en una base de datos. En este estado, el objeto no está disponible para su visualización o edición.<br/>                                                                                                                                                                                                                                   |
| Cargado<br/>  | Las estructuras de datos del objeto creadas por el controlador de objetos se encuentran en la memoria del contenedor. El contenedor ha establecido la comunicación con el controlador de objetos y hay datos de presentación en caché disponibles para representar el objeto. El controlador de objetos procesa las llamadas. Este estado, debido a su sobrecarga baja, se usa cuando un usuario simplemente está viendo o imprimiendo un objeto.<br/> |
| En ejecución<br/> | Se han creado los objetos que controlan la comunicación remota y se está ejecutando la aplicación de servidor OLE. Se puede tener acceso a las interfaces del objeto y el contenedor puede recibir notificaciones de cambios. En este estado, un usuario final puede editar o manipular de otro modo el objeto.<br/>                                                                                                                    |



 

Para obtener más información, vea los temas siguientes:

-   [Entrando en el estado cargado](entering-the-loaded-state.md)
-   [Entrar en el estado de ejecución](entering-the-running-state.md)
-   [Entrar en el estado pasivo](entering-the-passive-state.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 





