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
# <a name="implementing-register"></a><span data-ttu-id="c730c-104">Implementación del registro</span><span class="sxs-lookup"><span data-stu-id="c730c-104">Implementing Register</span></span>

<span data-ttu-id="c730c-105">Monitor de red carga una captura del archivo de captura y, a continuación, inicia una llamada a la función de [**registro**](register-parser.md) para todos los protocolos que puede identificar.</span><span class="sxs-lookup"><span data-stu-id="c730c-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="c730c-106">Cada DLL del analizador debe implementar una función de **registro** para cada protocolo que admita el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="c730c-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="c730c-107">Cada implementación de la función [**Register**](register-parser.md) debe llamar a las funciones [**CreatePropertyDatabase**](createpropertydatabase.md) y [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) para crear y rellenar la base de [*datos de propiedades*](p.md) para el protocolo y, a continuación, [**CreateHandoffTable**](createhandofftable.md) para crear la tabla de [*entrega*](h.md) para el protocolo, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c730c-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="c730c-108">Se definen las propiedades de protocolo para Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c730c-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="c730c-109">Las propiedades no se asignan a una ubicación en los datos de captura hasta que se llama a la función de exportación [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="c730c-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="c730c-110">En el procedimiento siguiente se identifican los pasos necesarios para implementar la función de [**registro**](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="c730c-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="c730c-111">**Para implementar el registro para un protocolo**</span><span class="sxs-lookup"><span data-stu-id="c730c-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="c730c-112">Defina una matriz de estructuras [**PROPERTYINFO**](propertyinfo.md) para describir cada una de las propiedades que admite el protocolo.</span><span class="sxs-lookup"><span data-stu-id="c730c-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="c730c-113">Llame a [**CreatePropertyDatabase**](createpropertydatabase.md) para proporcionar un identificador de protocolo y el número de propiedades que admite el protocolo.</span><span class="sxs-lookup"><span data-stu-id="c730c-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="c730c-114">Llame a [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) en un bucle para agregar cada propiedad definida en la matriz de estructuras [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c730c-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="c730c-115">Si el protocolo utiliza una tabla de entrega, llame a [**CreateHandoffTable**](createhandofftable.md), después de que todas las propiedades del Protocolo se agreguen a la base de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c730c-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="c730c-116">La siguiente es una implementación básica de [**Register**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="c730c-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="c730c-117">Tenga en cuenta que se crea una base de datos de propiedades para un protocolo que solo admite dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="c730c-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="c730c-118">Este ejemplo de código se toma del analizador genérico que proporciona Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c730c-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

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

 

 
