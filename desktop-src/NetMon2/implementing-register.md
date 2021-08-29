---
description: Monitor de red carga una captura desde el archivo de captura y, a continuación, comienza a llamar a la función Register para todos los protocolos que puede identificar. Cada ARCHIVO DLL del analizador debe implementar una función Register para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implementación del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74139dca6cdf4c70977dc1cc17428447eb10455c29d1f865a9cd2aa604eb08ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890455"
---
# <a name="implementing-register"></a>Implementación del registro

Monitor de red carga una captura desde el archivo de captura y, a continuación, comienza a llamar a la función [**Register**](register-parser.md) para todos los protocolos que puede identificar. Cada ARCHIVO DLL del analizador debe implementar una **función Register** para cada protocolo que admita el archivo DLL del analizador.

Cada implementación de la función [**Register**](register-parser.md) debe llamar a las funciones [](h.md) [**CreatePropertyDatabase**](createpropertydatabase.md) y [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) para crear y rellenar la base de datos de propiedades del protocolo y, a continuación, [**createHandoffTable**](createhandofftable.md) para crear la tabla de entrega para el protocolo, si es necesario. [](p.md)

> [!Note]  
> Las propiedades de protocolo se definen para Monitor de red. Las propiedades no se asignan a una ubicación en los datos de captura hasta que se llama a la función de exportación [**AttachProperties.**](attachproperties.md)

 

El procedimiento siguiente identifica los pasos necesarios para implementar la [**función Register.**](register-parser.md)

**Para implementar register para un protocolo**

1.  Defina una matriz de [**estructuras PROPERTYINFO**](propertyinfo.md) para describir cada propiedad que admite el protocolo.
2.  Llame [**a CreatePropertyDatabase**](createpropertydatabase.md) para proporcionar un identificador de protocolo y el número de propiedades que admite el protocolo.
3.  Llame [**a AddProperty**](/previous-versions/bb251873(v=msdn.10)) en un bucle para agregar cada propiedad definida en la [**matriz de estructura PROPERTYINFO.**](propertyinfo.md)
4.  Si el protocolo usa una tabla de entrega, llame a [**CreateHandoffTable,**](createhandofftable.md)después de agregar todas las propiedades del protocolo a la base de datos de propiedades.

A continuación se muestra una implementación básica de [**Register**](register-parser.md). Tenga en cuenta que se crea una base de datos de propiedades para un protocolo que solo admite dos propiedades. Este ejemplo de código se toma del analizador genérico que Monitor de red proporciona.

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
