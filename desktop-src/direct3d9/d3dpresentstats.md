---
description: Describe las estadísticas de cadena de intercambio relacionadas con las llamadas de PresentEx.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888681"
---
# <a name="d3dpresentstats-structure"></a>D3DPRESENTSTATS (estructura)

Describe las estadísticas de cadena de intercambio relacionadas con [**las llamadas de PresentEx.**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)

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



## <a name="members"></a>Members

<dl> <dt>

**PresentCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento en ejecución de llamadas present correctas realizadas por un dispositivo de visualización que se está generando actualmente en la pantalla. Este parámetro es realmente el identificador present de la última llamada present y no es necesariamente el número total de llamadas a Present API realizadas.

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

El recuento de vblank en el que se mostró el último presente en la pantalla, el recuento de vblank se incrementa una vez cada intervalo de vblank.

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

El recuento de vblank cuando el programador muestreó por última vez la hora de la máquina mediante una llamada a QueryPerformanceCounter.

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

Tipo: **[ **ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

La última hora de la máquina muestreada del programador, obtenida mediante una llamada a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

Tipo: **[ **ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando una aplicación 9Ex adopta el modo de volteo presente (D3DSWAPEFFECT FLIPEX), las aplicaciones pueden detectar la colocación de fotogramas llamando a \_ GetPresentStatistics en cualquier momento. En efecto, pueden hacer lo siguiente.

1.  Representación en el búfer de reserva
2.  Llamar a Present
3.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
4.  Representación del fotograma siguiente en el búfer de reserva
5.  Llamar a Present
6.  Repita los pasos 4 y 5 una o más veces.
7.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
8.  Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. La aplicación puede calcular el presentRefreshCount correspondiente de un parámetro PresentCount determinado en función de las suposiciones de incremento PresentRefreshCount y asignación presentCount de los objetos frame presentes. Si la última muestra de PresentRefreshCount no coincide con presentCount (es decir, si PresentRefreshCount se ha incrementado pero PresentCount no, se ha producido la colocación de fotogramas).

Las aplicaciones pueden determinar si se ha eliminado un fotograma mediante el muestreo de dos instancias de PresentCount y GetPresentStats (mediante una llamada a la API GetPresentStats en dos puntos cualquiera en el tiempo). Por ejemplo, una aplicación multimedia que se presenta a la misma velocidad que la frecuencia de actualización del monitor (por ejemplo, la frecuencia de actualización de supervisión es de 60Hz, la aplicación presenta un fotograma cada 1/60 segundos) quiere presentar fotogramas A, B, C, D, E, cada uno correspondiente a Present IDs (PresentCount) 1, 2, 3, 7, 8.

El código de la aplicación es similar a la secuencia siguiente.

1.  Representación del marco A en el búfer de reserva
2.  Call Present, PresentCount = 1
3.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
4.  Representar los 4 fotogramas siguientes, B, C, D, E, respectivamente
5.  Llamar a Present 4 veces, PresentCounts = 2, 3, 7, 8, respectivamente
6.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
7.  Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si la diferencia es 2, es decir, han transcurrido 2 intervalos de vblank entre las dos llamadas API GetPresentStats, el último fotograma presentado debe ser el fotograma C. Dado que la aplicación presenta un intervalo de vblank (la frecuencia de actualización del monitor), el tiempo transcurrido entre el momento en que se presenta el fotograma A y el momento en que se presenta el fotograma C debe ser de 2 vblanks.
8.  Compare los valores de PresentCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si el primer PresentCount es 1 (correspondiente al marco A) y el segundo PresentCount es 3 (correspondiente al marco C), no se han descartado fotogramas. Si el segundo PresentCount es 3, que corresponde al marco D, la aplicación sabe que se ha descartado un fotograma.

Tenga en cuenta que GetPresentStatistics se procesará después de llamarla, independientemente del estado de las llamadas PresentEx del modo FLIPEX.

**Windows Vista:** Las llamadas Present se pondrán en cola y, a continuación, se procesarán antes de que se procese la llamada a GetPresentStats.

Cuando una aplicación detecta que la presentación de determinados fotogramas está detrás, puede omitir esos fotogramas y corregir la presentación para volver a sincronizarla con la vblank. Para ello, una aplicación simplemente no puede representar los fotogramas en tiempo de espera y empezar a representar con el siguiente fotograma correcto en la cola. Sin embargo, si una aplicación ya ha iniciado la representación de fotogramas en tiempo de retraso, puede usar un nuevo parámetro Present en D3D9Ex denominado D3DPRESENT \_ FORCEIMMEDIATE. La marca se pasará en los parámetros de la llamada API Present e indica al tiempo de ejecución que el marco se procesará inmediatamente dentro del siguiente intervalo de vblank, no visible en la pantalla en absoluto. Este es el ejemplo de uso de la aplicación después del último paso del ejemplo anterior.

1.  Representación del fotograma siguiente en el búfer de reserva
2.  Descubra en PresentRefreshCount que el siguiente fotograma ya es tarde.
3.  Establezca Present interval en D3DPRESENT \_ FORCEIMMEDIATE
4.  Llamada a Present en el fotograma siguiente

Las aplicaciones pueden sincronizar secuencias de vídeo y audio de la misma manera porque el comportamiento de GetPresentStatistics no cambia en ese escenario.

El modo de volteo D3D9Ex proporciona información de estadísticas de fotogramas a las aplicaciones con ventanas y a las aplicaciones de pantalla completa 9Ex.

**Windows Vista:** Use las API de DWM para recuperar las estadísticas actuales.

Cuando Administrador de ventanas de escritorio está desactivado, las aplicaciones en modo de ventana 9Ex que usan el modo de volteo recibirán información de estadísticas presentes de precisión limitada.

**Windows Vista: **

Si una aplicación no es lo suficientemente rápida como para mantenerse al día con la frecuencia de actualización del monitor, posiblemente debido a un hardware lento o a la falta de recursos del sistema, puede experimentar un problema de gráficos. Un problema es un denominado problema visual. Si un monitor está configurado para actualizarse a 60 Hz y la aplicación solo puede administrar 30 fps, la mitad de los fotogramas tendrán problemas.

Las aplicaciones pueden detectar un problema si se realiza un seguimiento de SynchRefreshCount. Por ejemplo, una aplicación podría realizar la siguiente secuencia de acciones.

1.  Representar en el búfer de reserva.
2.  Llame a Present.
3.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
4.  Represente el fotograma siguiente en el búfer de reserva.
5.  Llame a Present.
6.  Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.
7.  Compare los valores de SyncRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas. Si la diferencia es mayor que una, se omitió un marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
