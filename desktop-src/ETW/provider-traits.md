---
description: Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Rasgos del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2131ee4900fca40b26e8675b3eb4aade4e740fd49d1ed06098a21682ed55ff25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069895"
---
# <a name="provider-traits"></a>Rasgos del proveedor

Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual. Se pueden usar para proveedores de seguimiento o basados en manifiestos. Actualmente, esto incluye compatibilidad para agregar un nombre de proveedor o un grupo de proveedores a un registro de proveedor individual. Es probable que se agregó más tipos de rasgos en el futuro. Esta información se almacena en el kernel como un blob binario de un formato de conjunto.

Los rasgos solo se pueden establecer una vez para un registro. Cualquier intento adicional de establecer los rasgos en ese registro producirá un error.

Para establecer Provider Traits en un proveedor basado en manifiesto, llame a la función [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la clase de información EventProviderSetTraits. El búfer EventInformation debe contener un blob binario con el formato siguiente:

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

A partir del rasgo individual, ETW \_ PROVIDER TRAIT TYPE se define \_ \_ como:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

Los proveedores de registro de seguimiento establecen automáticamente los rasgos de proveedor cuando se llama a la función [**TraceLoggingRegister.**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) El nombre del proveedor tracelogging siempre se incluirá en sus rasgos. Un grupo se puede establecer en un proveedor tracelogging mediante la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) en la definición del proveedor.

## <a name="custom-traits"></a>Rasgos personalizados

Aunque la mayoría de los 255 tipos de rasgos posibles aún no están definidos, microsoft reserva los tipos de rasgos del 1 al 127 para su definición. Los desarrolladores externos pueden usar los valores de tipo indexados más altos restantes como es conveniente. Cualquier persona que considere la posibilidad de agregar sus propios rasgos personalizados a su proveedor debe intentar mantener su tamaño total de rasgos por debajo de 256 bytes por los siguientes motivos:

-   Los rasgos se incluyen en todos los eventos escritos para el proveedor. Los rasgos grandes podrían dar lugar a archivos de registro muy grandes.
-   Los rasgos se almacenan en un grupo de kernels sin página durante la vigencia del proveedor.

## <a name="provider-groups"></a>Grupos de proveedores

Un grupo de proveedores es una entidad controlable definida por GUID muy parecido a un propio proveedor. La diferencia clave es que, aunque se usa un GUID de proveedor para controlar los registros de solo su proveedor, un grupo controlará todos sus registros de miembros. Por ejemplo, al habilitar un grupo de proveedores con una palabra clave y un nivel determinados, se habilitarán todos los registros de miembros de grupos con esa palabra clave y nivel.

La pertenencia a grupos puede estar restringida por permisos. Si el llamador [**de EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) no tiene permisos para unirse al grupo especificado, se denegará la pertenencia.

En algunos casos, es posible que el controlador de sesión de seguimiento quiera excluir algunos proveedores de su habilitación de un grupo. Esto se puede hacer estableciendo una lista de no permitir. Una lista de no permitidos es una lista de GUID de proveedor que no se habilitarán en función de la configuración del grupo para una sola sesión de registro. Las listas no se pueden cambiar dinámicamente [**con TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y la clase de información TraceSetDisallowList.

Aunque la mayoría de las acciones de habilitación se pueden realizar para grupos de proveedores de forma similar a los proveedores individuales, hay algunas excepciones. Entre las excepciones se incluyen:

-   Las sesiones de seguimiento privadas no pueden controlar los grupos de proveedores.
-   Los filtros Nombre de evento, Id. de evento y Carga útil no son aplicables a los grupos de proveedores, ya que asumen información específica de un proveedor individual.

 

 
