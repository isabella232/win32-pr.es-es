---
title: Encabezado
description: El encabezado siguiente representa uno de los estilos de encabezado que puede generar la versión actual de MIDL. Para mayor comodidad, aquí se proporciona la lista completa de campos de encabezado.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ee00425f3611234b0cd001f254b1499a0d4873d05846c65a2828c3eeffe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924544"
---
# <a name="the-header"></a>Encabezado

El encabezado siguiente representa uno de los estilos de encabezado que puede generar la versión actual de MIDL. Para mayor comodidad, aquí se proporciona la lista completa de campos de encabezado.

([**encabezado –Oif)**](/windows/desktop/Midl/-oi)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Extensiones a partir de Windows 2000: <8> para 32 bits, <12> para 64 bits)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

La versión \_ de<1> proporciona el tamaño de la sección de extensión, en bytes. De este modo, el motor EXPLORE actual puede ir paso a paso por la sección de extensión correctamente incluso si la sección procede de una versión posterior del compilador con más campos de los que entiende el motor actual.

INTERPRETER \_ OPT \_ FLAGS2 se define de la siguiente manera:

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

El **miembro HasNewCorrDesc** indica si se usan nuevos descriptores de correlación en las cadenas de formato generadas por el compilador. El nuevo descriptor de correlación está relacionado con la funcionalidad de denegación de ataque. Los **miembros ClientCorrCheck y** **ServerCorrCheck** se establecen cuando la rutina necesita la comprobación de correlación en el lado indicado.

Las **marcas HasNotify** y **HasNotify2** indican que la rutina usa la característica de notificación definida por los atributos de marca **\[ notify \]** y **\[ notify, \_ \]** respectivamente.

El **miembro ClientCorrCheck es** una sugerencia de tamaño de caché en el lado cliente y **ServerCorrCheck** es una sugerencia en el lado servidor. Cuando el tamaño sale como cero, se debe usar un tamaño predeterminado.

El **elemento NotifyIndex** es un índice de una rutina de notificación, si se usa uno.

El **elemento FloatDoubleMask** aborda el problema de un argumento de punto flotante para los archivos de 64 Windows. Este campo solo se genera para códigos auxiliares de 64 bits. La máscara es necesaria para las rutinas de ensamblado que descargan o cargan registros desde o hacia la pila virtual para controlar los argumentos de punto flotante y los registros correctamente. La máscara consta de 2 bits por argumento o, en su lugar, por registro de punto flotante. La codificación es la siguiente: los bits menos significativos corresponden al primer registro FP, los 2 bits siguientes corresponden al segundo registro, y así sucesivamente.

> [!Note]  
> Para las rutinas de objeto, el primer argumento termina en el segundo registro debido a que este puntero es el primero. Para cada registro, el significado de los bits es como se muestra en la tabla siguiente.

 



| Bits | Significado                                          |
|------|--------------------------------------------------|
| 01   | Se debe cargar un valor float en el registro.  |
| 10   | Se debe cargar un valor double en el registro. |



 

00 y 11 son valores no válidos para los bits.

Actualmente hay ocho registros FP en un procesador intel architecture de 64 bits, por lo que la máscara solo puede tener establecidos 16b bits más bajos. El tamaño de máscara se ha establecido en un total de 16 bits en función de que la máscara del compilador de C permanece sin cambios.

## <a name="header-streamlining-for-performance"></a>Secuenciación de encabezados para el rendimiento

Para simplificar el código y mejorar el rendimiento, el compilador intenta generar un encabezado de tamaño fijo siempre que sea posible. En concreto, se usa el siguiente encabezado para DCOM asincrónico:

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 