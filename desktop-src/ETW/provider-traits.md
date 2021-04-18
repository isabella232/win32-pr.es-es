---
description: Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Rasgos de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985858"
---
# <a name="provider-traits"></a>Rasgos de proveedor

Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual. Se pueden usar para los proveedores de TraceLogging o basados en manifiestos. Esto incluye actualmente compatibilidad para agregar un nombre de proveedor o un grupo de proveedores a un registro de proveedor individual. Es probable que se agreguen más tipos de rasgos en el futuro. Esta información se almacena en el kernel como un BLOB binario con un formato de conjunto.

Los rasgos solo se pueden establecer una vez para un registro. Se producirá un error en cualquier intento adicional de establecer los rasgos en ese registro.

Para establecer rasgos de proveedor en un proveedor basado en manifiesto, llame a la función [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la clase de información EventProviderSetTraits. El búfer de EventInformation debe contener un BLOB binario con el siguiente formato:

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

Los rasgos individuales deben tener el formato siguiente:

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

Desde el rasgo individual, el \_ tipo de rasgo del proveedor ETW \_ \_ se define como:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

Los proveedores de TraceLogging establecen automáticamente los rasgos de proveedor cuando se llama a la función [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) . El nombre del proveedor de TraceLogging siempre se incluirá en sus rasgos. Se puede establecer un grupo en un proveedor TraceLogging mediante la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) en la definición del proveedor.

## <a name="custom-traits"></a>Rasgos personalizados

Aunque la mayoría de los tipos de rasgos posibles de 255 aún no se han definido, los tipos de rasgos 1-127 están reservados para la definición de Microsoft. Los desarrolladores externos pueden usar los valores de tipo indizados más altos, tal y como se ven. Cualquier persona que considere agregar sus propios rasgos personalizados a su proveedor debe intentar mantener su tamaño total de rasgos en 256 bytes por los siguientes motivos:

-   Los rasgos se incluyen en cada evento escrito para el proveedor. Los rasgos grandes pueden dar lugar a archivos de registro de gran tamaño.
-   Los rasgos se almacenan en un grupo de kernel no paginado durante la vigencia del proveedor.

## <a name="provider-groups"></a>Grupos de proveedores

Un grupo de proveedores es una entidad controlable por GUID muy similar a la de un proveedor. La principal diferencia es que, mientras que un GUID de proveedor se utiliza para controlar los registros de solo su proveedor, un grupo controlará todos sus registros de miembros. Por ejemplo, si se habilita un grupo de proveedores con una palabra clave y un nivel determinados, se habilitarán todos los registros de miembros de grupos con esa palabra clave y el nivel.

La pertenencia a grupos puede estar restringida por permisos. Si el autor de la llamada de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) no tiene permisos para unirse al grupo especificado, se denegará la pertenencia.

En algunos casos, es posible que el controlador de sesión de seguimiento desee excluir algunos proveedores de la habilitación de un grupo. Esto puede hacerse mediante la configuración de una lista de deshabilitación. Una lista de no permitidos es una lista de GUID de proveedor que no se habilitará en función de la configuración de grupo para una sesión de registro única. Las listas de no permitidos se pueden cambiar dinámicamente con [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y la clase de información TraceSetDisallowList.

Aunque la mayoría de las acciones de habilitación se pueden realizar para los grupos de proveedores de una manera similar a los proveedores individuales, hay algunas excepciones. Entre las excepciones se incluyen:

-   Los grupos de proveedores no se pueden controlar mediante sesiones de seguimiento privadas.
-   Los filtros nombre de evento, ID. de evento y carga no se aplican a los grupos de proveedores cuando asumen información específica de un proveedor individual.

 

 
