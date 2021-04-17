---
title: Anotaciones de encabezado
description: Las anotaciones de encabezado describen cómo una función usa sus parámetros y el valor devuelto.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Anotaciones del archivo de encabezado de la API de Windows
- anotaciones del archivo de encabezado
- Specstrings. h
- lenguaje de anotación estándar (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714430"
---
# <a name="header-annotations"></a>Anotaciones de encabezado

\[En este tema se describen las anotaciones admitidas en los encabezados de Windows a través de Windows 7. Si va a desarrollar para Windows 8, debe usar las anotaciones descritas en [anotaciones de sal]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

Las anotaciones de encabezado describen cómo una función usa sus parámetros y el valor devuelto. Estas anotaciones se han agregado a muchos de los archivos de encabezado de Windows para ayudarle a asegurarse de que está llamando correctamente a la API de Windows. Si habilita el análisis de código, que está disponible a partir de Visual Studio 2005, el compilador producirá advertencias de nivel 6000 si no está llamando a estas funciones según el uso descrito a través de las anotaciones. También puede agregar estas anotaciones en su propio código para asegurarse de que se llama correctamente. Para habilitar el análisis de código en Visual Studio, consulte la documentación de su versión de Visual Studio.

Estas anotaciones se definen en Specstrings. h. Se basan en primitivos que forman parte del lenguaje de anotación estándar (SAL) y se implementan mediante `_declspec("SAL_*")` .

Hay dos clases de anotaciones: anotaciones de búfer y anotaciones avanzadas.

## <a name="buffer-annotations"></a>Anotaciones de búfer

Las anotaciones de búfer describen cómo las funciones usan sus punteros y se pueden usar para detectar saturaciones del búfer. Cada parámetro puede usar una anotación de búfer o cero. Una anotación de búfer se construye con un carácter de subrayado inicial y los componentes descritos en las secciones siguientes.



| Tamaño de búfer                                                                                  | Descripción                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*tamaño*)<br/>                        | Especifica el tamaño total del búfer. Se usa con \_ BCOUNT y \_ ecount; no se usa con \_ Part. Este valor es el espacio accesible; puede ser menor que el espacio asignado.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*tamaño*,*longitud*)<br/> | Especifica el tamaño total y la longitud inicializada del búfer. Se usa con \_ BCOUNT \_ Part y \_ ecount \_ Part. El tamaño total puede ser menor que el espacio asignado.<br/>              |



 



| Unidades de tamaño de búfer                                                       | Descripción                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | El tamaño del búfer está en bytes.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | El tamaño del búfer está en elementos.<br/> |



 



| Dirección                                                            | Descripción                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_de<br/>          | La función Lee del búfer. El autor de la llamada proporciona el búfer y lo inicializa.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_Inout<br/> | La función Lee y escribe en el búfer. El autor de la llamada proporciona el búfer y lo inicializa. Si se usa con \_ deref, la función puede reasignar el búfer.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_enuncia<br/>       | La función escribe en el búfer. Si se usa en el valor devuelto o con \_ deref, la función proporciona el búfer y lo inicializa. De lo contrario, el autor de la llamada proporciona el búfer y la función lo inicializa.<br/> |



 



| Direccionamiento indirecto                                                                       | Descripción                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_deref<br/>              | Desreferenciar el parámetro para obtener el puntero de búfer. Este parámetro no puede ser **null**.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ OPT<br/> | Desreferenciar el parámetro para obtener el puntero de búfer. Este parámetro puede ser **NULL**.<br/>     |



 



| Inicialización                                                    | Descripción                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_total<br/> | La función inicializa todo el búfer. Use solo con búferes de salida.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_referencia<br/> | La función inicializa parte del búfer y indica de forma explícita cuánto. Use solo con búferes de salida.<br/> |



 



| Búfer requerido u opcional                                    | Descripción                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_rechace<br/> | Este parámetro puede ser **NULL**.<br/> |



 

En el ejemplo siguiente se muestran las anotaciones de la función **GetModuleFileName** . El parámetro *hModule* es un parámetro de entrada opcional. El parámetro *lpFilename* es un parámetro de salida; su tamaño en caracteres se especifica mediante el parámetro *nSize* y su longitud incluye el carácter de terminación **null**. El parámetro *nSize* es un parámetro de entrada.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



A continuación se enumeran las anotaciones definidas en Specstrings. h. Utilice la información de las tablas anteriores para interpretar su significado.

__bcount (*tamaño*)  
__bcount_opt (*tamaño*)  
__deref_bcount (*tamaño*)  
__deref_bcount_opt (*tamaño*)  
__deref_ecount (*tamaño*)  
__deref_ecount_opt (*tamaño*)  
__deref_in  
__deref_in_bcount (*tamaño*)  
__deref_in_bcount_opt (*tamaño*)  
__deref_in_ecount (*tamaño*)  
__deref_in_ecount_opt (*tamaño*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*tamaño*)  
__deref_inout_bcount_full (*tamaño*)  
__deref_inout_bcount_full_opt (*tamaño*)  
__deref_inout_bcount_opt (*tamaño*)  
__deref_inout_bcount_part (*tamaño*,*longitud*)  
__deref_inout_bcount_part_opt (*tamaño*,*longitud*)  
__deref_inout_ecount (*tamaño*)  
__deref_inout_ecount_full (*tamaño*)  
__deref_inout_ecount_full_opt (*tamaño*)  
__deref_inout_ecount_opt (*tamaño*)  
__deref_inout_ecount_part (*tamaño*,*longitud*)  
__deref_inout_ecount_part_opt (*tamaño*,*longitud*)  
__deref_inout_opt  
__deref_opt_bcount (*tamaño*)  
__deref_opt_bcount_opt (*tamaño*)  
__deref_opt_ecount (*tamaño*)  
__deref_opt_ecount_opt (*tamaño*)  
__deref_opt_in  
__deref_opt_in_bcount (*tamaño*)  
__deref_opt_in_bcount_opt (*tamaño*)  
__deref_opt_in_ecount (*tamaño*)  
__deref_opt_in_ecount_opt (*tamaño*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*tamaño*)  
__deref_opt_inout_bcount_full (*tamaño*)  
__deref_opt_inout_bcount_full_opt (*tamaño*)  
__deref_opt_inout_bcount_opt (*tamaño*)  
__deref_opt_inout_bcount_part (*tamaño*,*longitud*)  
__deref_opt_inout_bcount_part_opt (*tamaño*,*longitud*)  
__deref_opt_inout_ecount (*tamaño*)  
__deref_opt_inout_ecount_full (*tamaño*)  
__deref_opt_inout_ecount_full_opt (*tamaño*)  
__deref_opt_inout_ecount_opt (*tamaño*)  
__deref_opt_inout_ecount_part (*tamaño*,*longitud*)  
__deref_opt_inout_ecount_part_opt (*tamaño*,*longitud*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*tamaño*)  
__deref_opt_out_bcount_full (*tamaño*)  
__deref_opt_out_bcount_full_opt (*tamaño*)  
__deref_opt_out_bcount_opt (*tamaño*)  
__deref_opt_out_bcount_part (*tamaño*,*longitud*)  
__deref_opt_out_bcount_part_opt (*tamaño*,*longitud*)  
__deref_opt_out_ecount (*tamaño*)  
__deref_opt_out_ecount_full (*tamaño*)  
__deref_opt_out_ecount_full_opt (*tamaño*)  
__deref_opt_out_ecount_opt (*tamaño*)  
__deref_opt_out_ecount_part (*tamaño*,*longitud*)  
__deref_opt_out_ecount_part_opt (*tamaño*,*longitud*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*tamaño*)  
__deref_out_bcount_full (*tamaño*)  
__deref_out_bcount_full_opt (*tamaño*)  
__deref_out_bcount_opt (*tamaño*)  
__deref_out_bcount_part (*tamaño*,*longitud*)  
__deref_out_bcount_part_opt (*tamaño*,*longitud*)  
__deref_out_ecount (*tamaño*)  
__deref_out_ecount_full (*tamaño*)  
__deref_out_ecount_full_opt (*tamaño*)  
__deref_out_ecount_opt (*tamaño*)  
__deref_out_ecount_part (*tamaño*,*longitud*)  
__deref_out_ecount_part_opt (*tamaño*,*longitud*)  
__deref_out_opt  
__ecount (*tamaño*)  
__ecount_opt (*tamaño*)  
__in  
__in_bcount (*tamaño*)  
__in_bcount_opt (*tamaño*)  
__in_ecount (*tamaño*)  
__in_ecount_opt (*tamaño*)  
__in_opt  
__inout  
__inout_bcount (*tamaño*)  
__inout_bcount_full (*tamaño*)  
__inout_bcount_full_opt (*tamaño*)  
__inout_bcount_opt (*tamaño*)  
__inout_bcount_part (*tamaño*,*longitud*)  
__inout_bcount_part_opt (*tamaño*,*longitud*)  
__inout_ecount (*tamaño*)  
__inout_ecount_full (*tamaño*)  
__inout_ecount_full_opt (*tamaño*)  
__inout_ecount_opt (*tamaño*)  
__inout_ecount_part (*tamaño*,*longitud*)  
__inout_ecount_part_opt (*tamaño*,*longitud*)  
__inout_opt  
__out  
__out_bcount (*tamaño*)  
__out_bcount_full (*tamaño*)  
__out_bcount_full_opt (*tamaño*)  
__out_bcount_opt (*tamaño*)  
__out_bcount_part (*tamaño*,*longitud*)  
__out_bcount_part_opt (*tamaño*,*longitud*)  
__out_ecount (*tamaño*)  
__out_ecount_full (*tamaño*)  
__out_ecount_full_opt (*tamaño*)  
__out_ecount_opt (*tamaño*)  
__out_ecount_part (*tamaño*,*longitud*)  
__out_ecount_part_opt (*tamaño*,*longitud*)  
__out_opt  

## <a name="advanced-annotations"></a>Anotaciones avanzadas

Las anotaciones avanzadas proporcionan información adicional sobre el parámetro o el valor devuelto. Cada parámetro o valor devuelto puede usar cero o una anotación avanzada.



| Anotación                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_bloqueos (*recurso*)<br/> | Las funciones se bloquean en el recurso especificado.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_regreso<br/>                                                                        | La función se puede usar como un puntero de función.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | Los llamadores deben comprobar el valor devuelto.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_cadena de formato \_<br/>                                                        | El parámetro es una cadena que contiene marcadores% de estilo printf.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_en \_ awcount (*expr*,*size*)<br/>                            | Si la expresión es true en la salida, el tamaño del búfer de entrada se especifica en bytes. Si la expresión es false, el tamaño se especifica en elementos.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | Se puede tener acceso al búfer hasta e incluir la primera secuencia de dos caracteres **nulos** o punteros.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | Se puede tener acceso al búfer hasta el primer carácter o puntero **nulo** o incluirlo.<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)<br/>                         | Si la expresión es true en la salida, el tamaño del búfer de salida se especifica en bytes. Si la expresión es false, el tamaño se especifica en elementos. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_estima<br/>                                                                        | Especifica el comportamiento de invalidación de estilo C# para los métodos virtuales.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_sector<br/>                                                                        | El parámetro está reservado para un uso futuro y debe ser cero o **null**.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_correcto (*expr*)<br/>                                                       | Si la expresión es true en la salida, el autor de la llamada puede confiar en todas las garantías especificadas por otras anotaciones. Si la expresión es falsa, el autor de la llamada no puede confiar en las garantías. Esta anotación se agrega automáticamente a las funciones que devuelven un valor **HRESULT** .<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Trate el parámetro como el tipo especificado en lugar de su tipo declarado.<br/>                                                                                                                                                                                             |



 

En los siguientes ejemplos se muestra el búfer y las anotaciones avanzadas para las funciones [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)y [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anotaciones SAL](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Tutorial: Analizar código de C/C++ en previsión de defectos](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

