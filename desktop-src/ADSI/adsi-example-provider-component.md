---
title: Componente de proveedor de ejemplo ADSI
description: Active Directory los escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe el componente de proveedor de ejemplo ADSI en profundidad.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356716"
---
# <a name="adsi-example-provider-component"></a>Componente de proveedor de ejemplo ADSI

Active Directory los escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe el componente de proveedor de ejemplo ADSI en profundidad. Los escritores de proveedores ADSI pueden instalar el proveedor de ejemplo y usar el marco de código como base para crear su propia implementación. Se tratan los temas siguientes:

[La instalación del componente de proveedor de ejemplo](installing-the-example-provider-component.md) describe cómo instalar el proveedor de ejemplo ADSI y su directorio ficticio. En esta sección se incluye una lista de los valores del registro.

[Definición de directorio](directory-definition.md) describe las entradas de directorio definidas por el componente de proveedor de ejemplo.

La [Administración de esquemas](schema-management.md) describe cómo cada elemento del servicio de directorio del componente de proveedor de ejemplo se puede representar mediante un tipo específico de Active Directory objeto.

[Enlazar a un objeto de Active Directory](binding-to-an-active-directory-object.md) describe cómo, dada una cadena ADsPath, el componente proveedor de ejemplo identifica ese elemento, crea el tipo adecuado de Active Directory objeto para él y recupera el tipo de puntero de interfaz solicitado en ese objeto para devolverlo al software cliente de ADS.

[Objetos de enumerador](enumerator-objects.md) muestra los tipos de enumeraciones específicos proporcionados por el componente de proveedor de ejemplo y en qué código fuente se pueden encontrar las implementaciones.

[Información general de código](code-overview.md) proporciona una descripción de nivel de tarea de cada parte del componente de proveedor de ejemplo.

[Detalles de código](code-details.md) enumera los módulos de software y su contenido.

 

 




