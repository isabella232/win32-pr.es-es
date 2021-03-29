---
title: El encabezado
description: El encabezado siguiente representa uno de los estilos de encabezado que puede generar la versión actual de MIDL. Para mayor comodidad, aquí se proporciona la lista completa de campos de encabezado.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afcc9ad880278fdbcb8efc45fdabdc22ad06224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904787"
---
# <a name="the-header"></a>El encabezado

El encabezado siguiente representa uno de los estilos de encabezado que puede generar la versión actual de MIDL. Para mayor comodidad, aquí se proporciona la lista completa de campos de encabezado.

([**–**](/windows/desktop/Midl/-oi) Encabezado de interfaces)

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

La \_ versión de la extensión<1> proporciona el tamaño de la sección de extensión, en bytes. Si lo hace, el motor NDR actual puede desplazarse por la sección de la extensión correctamente aunque la sección proviniera de una versión posterior del compilador con más campos de los que el motor actual entiende.

El intérprete \_ OPT \_ FLAGS2 se define de la siguiente manera:

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

El miembro **HasNewCorrDesc** indica si se usan nuevos descriptores de correlación en las cadenas de formato generadas por el compilador. El nuevo descriptor de correlación está relacionado con la funcionalidad de denegación de ataque. Los miembros **ClientCorrCheck** y **ServerCorrCheck** se establecen cuando la rutina necesita la comprobación de correlación en el lado indicado.

Las marcas **HasNotify** y **HasNotify2** indican que la rutina utiliza la característica de notificación, tal como se define en los atributos **\[ \] Notify** y **\[ Notify \_ Flag \]** , respectivamente.

El miembro **ClientCorrCheck** es una sugerencia de tamaño de caché en el lado cliente y **ServerCorrCheck** es una sugerencia en el lado servidor. Cuando el tamaño llega como cero, se debe usar un tamaño predeterminado.

El elemento **NotifyIndex** es un índice de una rutina Notify, si se usa una.

El elemento **FloatDoubleMask** aborda el problema de un argumento de punto flotante para Windows de 64 bits. Este campo solo se genera para el código auxiliar de 64 bits. La máscara es necesaria para las rutinas de ensamblado que descargan o cargan registros de/en la pila virtual para controlar los argumentos de punto flotante y se registran correctamente. La máscara consta de 2 bits por argumento, o en lugar de registro de punto flotante. La codificación es la siguiente: los bits menos significativos corresponden al primer registro FP, los dos bits siguientes corresponden al segundo registro, etc.

> [!Note]  
> En el caso de las rutinas de objeto, el primer argumento termina en el segundo registro debido a que este puntero está en primer lugar. En cada registro, el significado de bits es como se muestra en la tabla siguiente.

 



| Bits | Significado                                          |
|------|--------------------------------------------------|
| 01   | Un valor Float debe cargarse en el registro.  |
| 10   | Se debe cargar un valor Double en el registro. |



 

00 y 11 son valores no válidos para los bits.

Actualmente hay ocho registros FP en un procesador de 64 bits de arquitectura Intel, por lo que la máscara solo puede tener conjuntos de bits inferiores de 16B. El tamaño de la máscara se ha establecido en un total de 16 bits en función de la máscara del compilador de C que permanece sin cambios.

## <a name="header-streamlining-for-performance"></a>Optimización del encabezado para el rendimiento

Para simplificar el código y mejorar el rendimiento, el compilador intenta generar un encabezado de tamaño fijo siempre que sea posible. En concreto, se usa el encabezado siguiente para DCOM de Async:

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

 

 