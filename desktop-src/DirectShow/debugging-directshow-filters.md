---
description: Muchas de las funciones de depuración que se describen en este tema se implementan en la biblioteca de clases base de DirectShow. Para obtener más información, vea clases base de DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Depurar filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538068"
---
# <a name="debugging-directshow-filters"></a>Depurar filtros de DirectShow

Muchas de las funciones de depuración que se describen en este tema se implementan en la biblioteca de clases base de DirectShow. Para obtener más información, vea [clases base de DirectShow](directshow-base-classes.md).

## <a name="assertion-checking"></a>Comprobación de aserciones

Usar la comprobación de aserción libremente. Las aserciones pueden comprobar las suposiciones que se realizan en el código sobre las condiciones previas y posteriores. DirectShow proporciona varias macros de aserción. Para obtener más información, vea [macros Assert y Breakpoint](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Nombres de objeto

En las compilaciones de depuración, hay una lista global de objetos que derivan de la clase [**CBaseObject**](cbaseobject.md) . A medida que se crean objetos, se agregan a la lista. Cuando se destruyen, se quitan de la lista. Para mostrar una lista de esos objetos, llame a la función [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .

El método constructor para la clase base [**CBaseObject**](cbaseobject.md) (y la mayoría de las clases derivadas de ella) incluye un parámetro para el nombre del objeto. Asigne nombres únicos a sus objetos para identificarlos. Use la macro [**Name**](name.md) al declarar el nombre, de modo que el nombre se asigne solo en las compilaciones de depuración. En las compilaciones comerciales, el nombre se convierte en **null**.

## <a name="debug-logging"></a>Depurar registro

La función [**DbgLog**](dbglog.md) muestra los mensajes de depuración cuando se ejecuta el programa. Utilice esta función para realizar un seguimiento de la ejecución de la aplicación o el filtro. Puede registrar los códigos de retorno, los valores de las variables y cualquier otra información relevante.

Cada mensaje de depuración tiene un tipo, como un registro de \_ seguimiento o \_ un error de registro, y un nivel de depuración, que indica la importancia del mensaje. Los mensajes con niveles de depuración inferiores son más importantes que los de niveles superiores.

En el ejemplo siguiente, un filtro hipotético desconecta un PIN de una matriz de clavijas. Si el intento de desconexión se realiza correctamente, el filtro muestra un mensaje de seguimiento de registro \_ . Si se produce un error en el intento, se muestra un mensaje de error de registro \_ :


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



Al depurar, puede establecer el nivel de depuración para cada tipo de mensaje. Además, cada módulo (DLL o ejecutable) mantiene sus propios niveles de depuración. Si está probando un filtro, aumente los niveles de depuración para el archivo DLL que contiene el filtro.

Para obtener más información, vea [funciones de salida de depuración](debug-output-functions.md).

## <a name="critical-sections"></a>Secciones críticas

Para facilitar el seguimiento de los interbloqueos, incluya aserciones que determinen si el código de llamada posee una sección crítica determinada. Las funciones [**CritCheckIn**](critcheckin.md) y [**CritCheckOut**](critcheckout.md) indican si el subproceso que realiza la llamada es el propietario de una sección crítica. Normalmente, se llamaría a estas funciones desde una macro Assert.

También puede usar la función [**DbgLockTrace**](dbglocktrace.md) para realizar un seguimiento cuando se mantienen o liberan secciones críticas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar en DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



