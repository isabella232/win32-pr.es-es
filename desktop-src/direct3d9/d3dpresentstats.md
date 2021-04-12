---
description: Describe las estadísticas de intercambio relacionadas con las llamadas a PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Estructura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280372"
---
# <a name="d3dpresentstats-structure"></a>Estructura D3DPRESENTSTATS

Describe las estadísticas de intercambio relacionadas con las llamadas a [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PresentCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Se está ejecutando el recuento de las llamadas presentes correctas realizadas por un dispositivo de pantalla que actualmente se está mostrando en la pantalla. Este parámetro es realmente el identificador actual de la última llamada presente y no es necesariamente el número total de llamadas API presentes realizadas.

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

El recuento de VBlank en el que se mostró el último presente en la pantalla, el recuento de VBlank se incrementa una vez cada intervalo de VBlank.

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

El recuento de VBlank cuando el programador muestrea por última vez la hora del equipo mediante una llamada a QueryPerformanceCounter.

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

La última hora del equipo muestreada del programador, obtenida llamando a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando una aplicación 9Ex adopta el modo de volteo presente (D3DSWAPEFFECT \_ FLIPEX), las aplicaciones pueden detectar la caída de fotogramas llamando a GetPresentStatistics en cualquier momento. En efecto, pueden hacer lo siguiente.

1.  Representar en el búfer de reserva
2.  Llamar a present
3.  Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante
4.  Representar el siguiente fotograma en el búfer de reserva
5.  Llamar a present
6.  Repita los pasos 4 y 5 1 o más veces
7.  Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante
8.  Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. La aplicación puede calcular el PresentRefreshCount correspondiente de un parámetro PresentCount determinado en función de las suposiciones de PresentRefreshCount incremento y PresentCount de la asignación de fotogramas. Si la última muestra de PresentRefreshCount no coincide con el PresentCount (es decir, si el PresentRefreshCount ha aumentado pero PresentCount no, entonces se ha descartado el marco).

Las aplicaciones pueden determinar si un fotograma se ha quitado mediante el muestreo de dos instancias de PresentCount y GetPresentStats (llamando a la API GetPresentStats en dos puntos en el tiempo). Por ejemplo, una aplicación multimedia que se presenta a la misma velocidad que la frecuencia de actualización del monitor (por ejemplo, la frecuencia de actualización del monitor es 60 Hz, la aplicación presenta un fotograma cada 1/60 segundos) desea presentar los fotogramas a, B, C, D, E, cada uno correspondiente a los identificadores presentes (PresentCount) 1, 2, 3, 7

El código de aplicación tiene un aspecto similar al de la siguiente secuencia.

1.  Representar el marco a en el búfer de reserva
2.  Call Present, PresentCount = 1
3.  Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante
4.  Representar los 4 fotogramas siguientes, B, C, D, E, respectivamente
5.  Llamar a present 4 veces, PresentCounts = 2, 3, 7, 8, respectivamente
6.  Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante
7.  Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si la diferencia es 2, es decir, ha transcurrido 2 intervalos de VBlank entre las dos llamadas a la API de GetPresentStats, el último fotograma presentado debe ser el fotograma C. Dado que la aplicación presenta un intervalo de VBlank (la frecuencia de actualización del monitor), el tiempo transcurrido entre el momento en que se presenta el marco A y el momento en que se presenta el fotograma C debe ser 2 vblanks.
8.  Compare los valores de PresentCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si el primer PresentCount es 1 (correspondiente al marco a) y el segundo PresentCount es 3 (correspondiente al marco C), no se ha quitado ningún fotograma. Si el segundo PresentCount es 3, que corresponde a Frame D, la aplicación sabe que se ha quitado un fotograma.

Tenga en cuenta que GetPresentStatistics se procesará después de llamarse, independientemente del estado de FLIPEX Mode PresentEx calls.

**Windows Vista:** Las llamadas presentes se pondrán en cola y se procesarán antes de que se procese la llamada a GetPresentStats.

Cuando una aplicación detecta que la presentación de determinados fotogramas está detrás, puede omitir esos marcos y corregir la presentación para volver a sincronizar con el VBlank. Para ello, una aplicación simplemente no puede representar los fotogramas finales y comenzar la representación con el siguiente marco correcto en la cola. Sin embargo, si una aplicación ya ha iniciado la representación de fotogramas en tiempo de ejecución, puede usar un nuevo parámetro presente en D3D9Ex denominado D3DPRESENT \_ FORCEIMMEDIATE. La marca se pasará en los parámetros de la llamada de API presente e indica al tiempo de ejecución que el marco se procesará inmediatamente dentro del intervalo de VBlank siguiente, de modo que no es visible en la pantalla. Este es el ejemplo de uso de la aplicación después del último paso del ejemplo anterior.

1.  Representar el siguiente fotograma en el búfer de reserva
2.  Detectar desde PresentRefreshCount que el siguiente fotograma ya está retrasado
3.  Establecer el intervalo presente en D3DPRESENT \_ FORCEIMMEDIATE
4.  Llamada presente en el siguiente fotograma

Las aplicaciones pueden sincronizar secuencias de audio y vídeo de la misma manera porque el comportamiento de GetPresentStatistics no cambia en ese escenario.

El modo Flip de D3D9Ex proporciona información de estadísticas de fotogramas para aplicaciones en ventanas y aplicaciones 9Ex de pantalla completa.

**Windows Vista:** Usar las API de DWM para recuperar estadísticas presentes.

Cuando Administrador de ventanas de escritorio está desactivado, las aplicaciones de modo de ventana 9Ex que usan el modo Flip recibirán información de estadísticas presentes de precisión limitada.

* * Windows Vista: * *

Si una aplicación no es lo suficientemente rápida como para mantenerse al día de la frecuencia de actualización del monitor, probablemente debido a un hardware lento o a la falta de recursos del sistema, puede experimentar un problema con los gráficos. Un problema es una llamada visual interrupción. Si un monitor está configurado para actualizar a 60 Hz y la aplicación solo puede administrar 30 fps, la mitad de los fotogramas tendrá problemas.

Las aplicaciones pueden detectar un problema realizando un seguimiento de SynchRefreshCount. Por ejemplo, una aplicación puede realizar la siguiente secuencia de acciones.

1.  Se representa en el búfer de reserva.
2.  Llame a Present.
3.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
4.  Representar el siguiente fotograma en el búfer de reserva.
5.  Llame a Present.
6.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
7.  Compare los valores de SyncRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si la diferencia es mayor que uno, se omitirá un fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
