---
title: Componente de proveedor de ejemplo adsi
description: Active Directory escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe en profundidad el componente proveedor de ejemplo ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ff1d998a9db620c6dc6fb4402f126f556c95a45d589410800ea9c4b335a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023903"
---
# <a name="adsi-example-provider-component"></a>Componente de proveedor de ejemplo adsi

Active Directory escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe en profundidad el componente proveedor de ejemplo ADSI. Los escritores de proveedores ADSI pueden instalar el proveedor de ejemplo y usar el marco de código como base para crear su propia implementación. Se tratan los temas siguientes:

[Al instalar el componente de proveedor de](installing-the-example-provider-component.md) ejemplo se describe cómo instalar el proveedor de ejemplo ADSI y su directorio ficticio. En esta sección se incluye una lista de la configuración del Registro.

[Definición de](directory-definition.md) directorio describe las entradas de directorio definidas por el componente de proveedor de ejemplo.

[Administración de](schema-management.md) esquemas describe cómo cada elemento del servicio de directorio de componentes del proveedor de ejemplo se puede representar mediante un tipo específico de Active Directory objeto.

El enlace a un objeto [Active Directory](binding-to-an-active-directory-object.md) describe cómo, dada una cadena ADsPath, el componente de proveedor de ejemplo identifica ese elemento, crea el tipo adecuado de objeto Active Directory para él y recupera el tipo solicitado de puntero de interfaz en ese objeto para devolverlo al software cliente de ADs.

[Objetos enumeradores](enumerator-objects.md) enumera los tipos específicos de enumeraciones proporcionados por el componente de proveedor de ejemplo y en qué código fuente se pueden encontrar las implementaciones.

[Información general del](code-overview.md) código proporciona una descripción de nivel de tarea de cada parte del componente de proveedor de ejemplo.

[Detalles del código](code-details.md) enumera los módulos de software y su contenido.

 

 




