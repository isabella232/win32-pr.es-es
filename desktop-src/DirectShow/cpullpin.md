---
description: La clase CPullPin proporciona compatibilidad con los pines de entrada que extrae datos a través de la interfaz IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: CPullPin (clase, Pullpin.h)
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
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330855"
---
# <a name="cpullpin-class"></a>CPullPin (clase)

![cpullpin (jerarquía de clases)](images/pulpin01.png)

La `CPullPin` clase proporciona compatibilidad con los pines de entrada que extrae datos a través de la interfaz [**IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Use esta clase si va a implementar un filtro que usa el modelo de extracción para solicitar datos del filtro ascendente. Para obtener más información, vea Data Flow en el filtro Graph modelo de extracción.

Esta clase no deriva de **CBasePin** ni implementa la interfaz [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) y algunos de los nombres de método entra en conflicto con **IPin,** por lo que se usa mejor como un objeto auxiliar dentro del pin. Para usar esta clase, haga lo siguiente:

1.  Derive una clase auxiliar de `CPullPin` y derive una clase de pin de entrada de **CBasePin**. Declare una instancia del objeto `CPullPin` como una variable miembro de la clase pin.
2.  Invalide [**el método CBasePin::CheckConnect para**](cbasepin-checkconnect.md) llamar a [**CPullPin::Conectar**](cpullpin-connect.md). Este método consulta el otro pin para **IAsyncReader.**
3.  Invalide [**el método CBasePin::BreakConnect para**](cbasepin-breakconnect.md) llamar a [**CPullPin::D isconnect**](cpullpin-disconnect.md).
4.  Invalide [**el método CBasePin::Active**](cbasepin-active.md) para llamar [**a CPullPin::Active**](cpullpin-active.md). Este método inicia un subproceso de trabajo que extrae muestras del filtro ascendente. Cuando se conectan los pines, puede especificar si desea que el subproceso de trabajo realice solicitudes de lectura asincrónicas o sincrónicas.
5.  Invalide [**el método CBasePin::Inactive**](cbasepin-inactive.md) para llamar [**a CPullPin::Inactive.**](cpullpin-inactive.md) Este método cierra el subproceso de trabajo.
6.  Implemente el método [**virtual puro CPullPin::Receive**](cpullpin-receive.md) para procesar muestras entrantes y entregarlas de nivel inferior.
7.  Para establecer las posiciones de detenerse e iniciar, o para buscar la secuencia, llame al [**método CPullPin::Seek.**](cpullpin-seek.md) Este método pausa el subproceso de trabajo y vacía el gráfico de filtro.
8.  Implemente los métodos [**virtuales puros CPullPin::EndOfStream**](cpullpin-endofstream.md), [**CPullPin::BeginFlush**](cpullpin-beginflush.md)y [**CPullPin::EndFlush,**](cpullpin-endflush.md) como se describe en los comentarios de esos métodos.
9.  Implemente el método [**CPullPin::OnError**](cpullpin-onerror.md) virtual puro para controlar los errores de streaming.



| Variables de miembro público                             | Descripción                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Puntero a la **interfaz IMemAllocator** del asignador de memoria.                   |
| Métodos públicos                                      | Descripción                                                                           |
| [**Activo**](cpullpin-active.md)                   | Crea un subproceso de trabajo que extrae datos del pin de salida.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Trunca un valor a un límite de alineación especificado.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Redondea un valor hasta un límite de alineación especificado.                                  |
| [**Conectar**](cpullpin-connect.md)                 | Completa una conexión al pin de salida.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Método constructor.                                                                   |
| [**~CPullPin**](cpullpin--cpullpin.md)             | Método destructor. Virtual.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negocia un asignador con el pin de salida. Virtual.                                 |
| [**Desconectar**](cpullpin-disconnect.md)           | Picos en la conexión con el pin de salida.                                             |
| [**Duration**](cpullpin-duration.md)               | Recupera la duración de la secuencia.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del pin de salida. |
| [**Inactivo**](cpullpin-inactive.md)               | Apaga el subproceso de trabajo que extrae datos del pin de salida.                     |
| [**Seek**](cpullpin-seek.md)                       | Establece las posiciones inicial y de parada de la secuencia.                                      |
| Métodos virtuales puros                                | Descripción                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informa al filtro propietario de que vacíe los filtros de nivel inferior.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informa al filtro propietario para finalizar una operación de vaciado.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Se llama después de que el objeto entregue el último ejemplo.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Se llama si se produce un error durante el streaming.                                           |
| [**Recibir**](cpullpin-receive.md)                 | Se llama cuando el objeto recibe un ejemplo multimedia del pin de salida.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




