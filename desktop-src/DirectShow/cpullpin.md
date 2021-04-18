---
description: La clase CPullPin proporciona compatibilidad con los pin de entrada que extraen datos a través de la interfaz IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Clase CPullPin (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3039f97ca7fda43e4ecc6bd4eae05fff2ce90e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680868"
---
# <a name="cpullpin-class"></a>Clase CPullPin

![jerarquía de clases cpullpin](images/pulpin01.png)

La `CPullPin` clase proporciona compatibilidad con los pin de entrada que extraen datos a través de la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Use esta clase si está implementando un filtro que usa el modelo de extracción para solicitar datos del filtro de nivel superior. Para obtener más información, vea flujo de datos en el gráfico de filtro y modelo de extracción.

Esta clase no se deriva de **CBasePin** ni implementa la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) , y algunos de los nombres de método entran en conflicto con **IPin**, por lo que se recomienda usar como un objeto auxiliar dentro del código PIN. Para usar esta clase, haga lo siguiente:

1.  Derive una clase auxiliar de `CPullPin` y derive una clase de clavija de entrada de **CBasePin**. Declare una instancia del `CPullPin` objeto como una variable miembro de la clase PIN.
2.  Invalide el método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para llamar a [**CPullPin:: Connect**](cpullpin-connect.md). Este método consulta el otro PIN para **IAsyncReader**.
3.  Invalide el método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para llamar a [**CPullPin::D Ulta**](cpullpin-disconnect.md).
4.  Invalide el método [**CBasePin:: Active**](cbasepin-active.md) para llamar a [**CPullPin:: Active**](cpullpin-active.md). Este método inicia un subproceso de trabajo que extrae ejemplos del filtro de nivel superior. Cuando se conectan los pin, puede especificar si desea que el subproceso de trabajo realice solicitudes de lectura asincrónica o sincrónica.
5.  Invalide el método [**CBasePin:: Inactive**](cbasepin-inactive.md) para llamar a [**CPullPin:: Inactive**](cpullpin-inactive.md). Este método cierra el subproceso de trabajo.
6.  Implemente el método [**CPullPin:: Receive**](cpullpin-receive.md) virtual puro para procesar los ejemplos entrantes y entregarlos de forma descendente.
7.  Para establecer las posiciones de detención e inicio, o para buscar el flujo, llame al método [**CPullPin:: Seek**](cpullpin-seek.md) . Este método pausa el subproceso de trabajo y vacía el gráfico de filtro.
8.  Implemente los métodos virtuales [**CPullPin:: EndOfStream**](cpullpin-endofstream.md), [**CPullPin:: BeginFlush**](cpullpin-beginflush.md)y [**CPullPin:: EndFlush**](cpullpin-endflush.md) puros, tal y como se describe en las notas para esos métodos.
9.  Implemente el método [**CPullPin:: OnError**](cpullpin-onerror.md) virtual puro para controlar los errores de streaming.



| Variables de miembro público                             | Descripción                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Puntero a la interfaz **IMemAllocator** del asignador de memoria.                   |
| Métodos públicos                                      | Descripción                                                                           |
| [**Activo**](cpullpin-active.md)                   | Crea un subproceso de trabajo que extrae datos del PIN de salida.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Trunca un valor en un límite de alineación especificado.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Redondea un valor hasta un límite de alineación especificado.                                  |
| [**Conectar**](cpullpin-connect.md)                 | Completa una conexión con el PIN de salida.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Método de constructor.                                                                   |
| [**~ CPullPin**](cpullpin--cpullpin.md)             | Método de destructor. Virtualiza.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negocia un asignador con el PIN de salida. Virtualiza.                                 |
| [**Desconectar**](cpullpin-disconnect.md)           | Appicos de la conexión con el PIN de salida.                                             |
| [**Duration**](cpullpin-duration.md)               | Recupera la duración de la secuencia.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del terminal de salida. |
| [**Inactivo**](cpullpin-inactive.md)               | Cierra el subproceso de trabajo que extrae datos del PIN de salida.                     |
| [**Seek**](cpullpin-seek.md)                       | Establece las posiciones de inicio y detención de la secuencia.                                      |
| Métodos virtuales puros                                | Descripción                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informa al filtro propietario de vaciar los filtros de nivel inferior.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informa al filtro propietario de que finalice una operación de vaciado.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Se llama después de que el objeto entregue el último ejemplo.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Se llama si se produce un error durante el streaming.                                           |
| [**Aparecen**](cpullpin-receive.md)                 | Se llama cuando el objeto recibe un ejemplo multimedia del terminal de salida.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




