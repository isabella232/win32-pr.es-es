---
title: Extensiones de esquema
description: La arquitectura del esquema ADSI proporciona que se pueden agregar nuevas clases de esquema al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7fdc4b363fea83029fc5526464bd5825fa851dbe82e874911a0ab45d869843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178824"
---
# <a name="schema-extensions"></a>Extensiones de esquema

La arquitectura del esquema ADSI proporciona que se pueden agregar nuevas clases de esquema al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución. Esta última capacidad no requiere código nuevo. Se trata de una característica importante para los espacios de nombres que permiten servicios de directorio extensibles. El componente de proveedor debe permitir esta extensibilidad y saber dónde acceder y almacenar la instancia de clase y los valores de sus propiedades. En un servicio de directorio extensible típico, esta información se almacena en la base de datos del servicio de directorio de la misma manera que cualquier otra clase de esquema y definiciones de propiedad.

> [!Note]  
> En la terminología de la interfaz COM, solo se pueden agregar propiedades a una clase de esquema existente, no a métodos. Agregar un nuevo método requeriría agregar una nueva implementación de ese método y, por tanto, requerir código adicional.

 

Para obtener un ejemplo de un esquema de proveedor específico, vea [Administración de esquemas.](schema-management.md)

 

 




