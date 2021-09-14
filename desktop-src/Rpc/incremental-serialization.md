---
title: Serialización incremental
description: Cuando se usa la serialización de estilo incremental, se suministran tres rutinas para manipular el búfer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244628"
---
# <a name="incremental-serialization"></a>Serialización incremental

Cuando se usa la serialización de estilo incremental, se suministran tres rutinas para manipular el búfer. Estas rutinas son: Alloc, Read y Write. La rutina Alloc asigna un búfer del tamaño necesario. La rutina Write escribe los datos en el búfer y la rutina Read recupera un búfer que contiene datos serializados. Una sola llamada de serialización puede realizar varias llamadas a estas rutinas.

El estilo incremental de serialización usa las rutinas siguientes:

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

A continuación se muestran los prototipos de las funciones Alloc, Read y Write que debe proporcionar:

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

La entrada State de un parámetro para las tres funciones es el puntero definido por la aplicación que se asoció al identificador de servicios de codificación. La aplicación puede usar este puntero para acceder a la estructura que contiene información específica de la aplicación, como un identificador de archivo o un puntero de secuencia. Tenga en cuenta que los códigos auxiliares no modifican el puntero State que no sea para pasarlo a las funciones Alloc, Read y Write. Durante la codificación, se llama a Alloc para obtener un búfer en el que se serializan los datos. A continuación, se llama a Write para permitir que la aplicación controle cuándo y dónde se almacenan los datos serializados. Durante la decodificación, se llama a Read para devolver el número solicitado de bytes de datos serializados desde donde la aplicación los almacena.

Una característica importante del estilo incremental es que el identificador mantiene el puntero de estado. Este puntero mantiene el estado y nunca lo tocan las funciones RPC, excepto cuando se pasa el puntero a la función Alloc, Write o Read. El identificador también mantiene un estado interno que permite codificar y descodificar varias instancias de tipo en el mismo búfer agregando relleno según sea necesario para la alineación. La [**función MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) restablece un identificador a su estado inicial para permitir la lectura o escritura desde el principio del búfer.

Las funciones Alloc y Write, junto con un puntero definido por la aplicación, están asociadas a un identificador de servicios de codificación mediante una llamada a la función [**MesEncodeIncrementalHandleCreate.**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) **MesEncodeIncrementalHandleCreate** asigna la memoria necesaria para el identificador y, a continuación, la inicializa.

La aplicación puede llamar a [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) para crear un identificador de descodificación, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) para reinicializar el identificador o [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del identificador. La función Read, junto con un parámetro definido por la aplicación, está asociada a un identificador de descodificación mediante una llamada a la rutina **MesDecodeIncrementalHandleCreate.** La función crea el identificador y lo inicializa.

Los parámetros UserState, Alloc, Write y Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) pueden ser **NULL** para indicar que no hay ningún cambio.

 

 




