---
description: Muchos de los recursos de depuración que se describen en este tema se implementan en la biblioteca DirectShow de clases base. Para obtener más información, vea DirectShow base de datos.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Depuración de DirectShow filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070008"
---
# <a name="debugging-directshow-filters"></a>Depuración de DirectShow filtros

Muchos de los recursos de depuración que se describen en este tema se implementan en la biblioteca DirectShow de clases base. Para obtener más información, [vea DirectShow Base Classes](directshow-base-classes.md).

## <a name="assertion-checking"></a>Comprobación de aserciones

Use la comprobación de aserción de forma libre. Las aserciones pueden comprobar las suposiciones que realice en el código sobre las condiciones previas y posteriores. DirectShow proporciona varias macros de aserción. Para obtener más información, vea [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Nombres de objeto

En las compilaciones de depuración, hay una lista global de objetos que derivan de la [**clase CBaseObject.**](cbaseobject.md) A medida que se crean objetos, se agregan a la lista. Cuando se destruyen, se quitan de la lista. Para mostrar una lista de esos objetos, llame a la [**función DbgDumpObjectRegister.**](dbgdumpobjectregister.md)

El método de constructor para la clase base [**CBaseObject**](cbaseobject.md) (y la mayoría de las clases derivadas de ella) incluye un parámetro para el nombre del objeto. Dé a los objetos nombres únicos para identificarlos. Use la [**macro NAME**](name.md) al declarar el nombre, de modo que el nombre se asigne solo en las compilaciones de depuración. En las compilaciones comerciales, el nombre se convierte en **NULL.**

## <a name="debug-logging"></a>Depurar registro

La [**función DbgLog**](dbglog.md) muestra mensajes de depuración a medida que se ejecuta el programa. Use esta función para hacer un seguimiento de la ejecución de la aplicación o el filtro. Puede registrar códigos de retorno, los valores de las variables y cualquier otra información pertinente.

Cada mensaje de depuración tiene un tipo, como LOG TRACE o LOG ERROR, y un nivel de depuración, que indica la \_ \_ importancia del mensaje. Los mensajes con niveles de depuración inferiores son más importantes que los que tienen niveles más altos.

En el ejemplo siguiente, un filtro hipotético desconecta un pin de una matriz de pines. Si el intento de desconexión se realiza correctamente, el filtro muestra un mensaje LOG \_ TRACE. Si se produce un error en el intento, muestra un mensaje LOG \_ ERROR:


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



Al depurar, puede establecer el nivel de depuración para cada tipo de mensaje. Además, cada módulo (DLL o ejecutable) mantiene sus propios niveles de depuración. Si va a probar un filtro, eleve los niveles de depuración para el archivo DLL que contiene el filtro.

Para obtener más información, vea [Depurar funciones de salida](debug-output-functions.md).

## <a name="critical-sections"></a>Secciones críticas

Para facilitar el seguimiento de los interbloqueos, incluya aserciones que determinen si el código de llamada posee una sección crítica determinada. Las [**funciones CritCheckIn**](critcheckin.md) y [**CritCheckOut**](critcheckout.md) indican si el subproceso que realiza la llamada posee una sección crítica. Normalmente, llamaría a estas funciones desde dentro de una macro de aserción.

También puede usar la función [**DbgLockTrace para**](dbglocktrace.md) realizar un seguimiento de cuándo se mantienen o liberan secciones críticas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración en DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



