---
description: Monitor de red carga una captura del archivo de captura y, a continuación, inicia una llamada a la función de registro para todos los protocolos que puede identificar. Cada DLL del analizador debe implementar una función de registro para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implementación del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678387"
---
# <a name="implementing-register"></a>Implementación del registro

Monitor de red carga una captura del archivo de captura y, a continuación, inicia una llamada a la función de [**registro**](register-parser.md) para todos los protocolos que puede identificar. Cada DLL del analizador debe implementar una función de **registro** para cada protocolo que admita el archivo DLL del analizador.

Cada implementación de la función [**Register**](register-parser.md) debe llamar a las funciones [**CreatePropertyDatabase**](createpropertydatabase.md) y [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) para crear y rellenar la base de [*datos de propiedades*](p.md) para el protocolo y, a continuación, [**CreateHandoffTable**](createhandofftable.md) para crear la tabla de [*entrega*](h.md) para el protocolo, si es necesario.

> [!Note]  
> Se definen las propiedades de protocolo para Monitor de red. Las propiedades no se asignan a una ubicación en los datos de captura hasta que se llama a la función de exportación [**AttachProperties**](attachproperties.md) .

 

En el procedimiento siguiente se identifican los pasos necesarios para implementar la función de [**registro**](register-parser.md) .

**Para implementar el registro para un protocolo**

1.  Defina una matriz de estructuras [**PROPERTYINFO**](propertyinfo.md) para describir cada una de las propiedades que admite el protocolo.
2.  Llame a [**CreatePropertyDatabase**](createpropertydatabase.md) para proporcionar un identificador de protocolo y el número de propiedades que admite el protocolo.
3.  Llame a [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) en un bucle para agregar cada propiedad definida en la matriz de estructuras [**PROPERTYINFO**](propertyinfo.md) .
4.  Si el protocolo utiliza una tabla de entrega, llame a [**CreateHandoffTable**](createhandofftable.md), después de que todas las propiedades del Protocolo se agreguen a la base de datos de propiedades.

La siguiente es una implementación básica de [**Register**](register-parser.md). Tenga en cuenta que se crea una base de datos de propiedades para un protocolo que solo admite dos propiedades. Este ejemplo de código se toma del analizador genérico que proporciona Monitor de red.

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

 

 
