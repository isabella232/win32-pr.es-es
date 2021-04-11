---
title: Extensiones de esquema
description: La arquitectura del esquema ADSI proporciona que las nuevas clases de esquema se pueden agregar al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148731"
---
# <a name="schema-extensions"></a>Extensiones de esquema

La arquitectura del esquema ADSI proporciona que las nuevas clases de esquema se pueden agregar al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución. Esta última capacidad no requiere ningún código nuevo. Se trata de una característica importante para los espacios de nombres que permiten servicios de directorio extensibles. El componente de proveedor debe permitir esta extensibilidad y saber dónde tener acceso y almacenar la instancia de clase y los valores de sus propiedades. En un servicio de directorio extensible típico, esta información se almacena en la base de datos del servicio de directorio de la misma manera que cualquier otra clase de esquema y definiciones de propiedad.

> [!Note]  
> En la terminología de la interfaz COM, solo se pueden agregar propiedades a una clase de esquema existente, no a métodos. Para agregar un nuevo método, es necesario agregar una nueva implementación de ese método y, por tanto, requerir código adicional.

 

Para obtener un ejemplo de un esquema de proveedor específico, consulte [Administración de esquemas](schema-management.md).

 

 




