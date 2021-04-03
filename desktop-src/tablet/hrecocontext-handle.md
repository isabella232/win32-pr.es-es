---
description: Un identificador HRECOCONTEXT se usa para agregar entradas manuscritas al contexto, realizar reconocimiento de tinta (de forma sincrónica o asincrónica), recuperar el resultado del reconocimiento y recuperar alternativas.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Identificador de HRECOCONTEXT (Resumen. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908033"
---
# <a name="hrecocontext-handle"></a>Identificador de HRECOCONTEXT

Un identificador **HRECOCONTEXT** se usa para agregar entradas manuscritas al contexto, realizar reconocimiento de tinta (de forma sincrónica o asincrónica), recuperar el resultado del reconocimiento y recuperar alternativas.

La razón principal para tener identificadores de contexto de reconocedor es diferenciar entre entradas de entrada manuscrita. Por ejemplo, puede crear una aplicación con dos ventanas, el usuario que puede realizar la entrada manuscrita en cualquier ventana. No desea que la tinta de la primera ventana se mezcle con la tinta de la segunda ventana cuando pide al reconocedor que reconozca la tinta de una de las ventanas. En este tipo de aplicación, se crean dos contextos de reconocedor (uno para cada ventana) y se agregan trazos que entran en la ventana 1 al contexto de reconocedor 1 y a los trazos de la ventana 2 al contexto de reconocedor 2. Para devolver los resultados del reconocimiento, llame al proceso en el contexto de reconocedor 1 o en el contexto del reconocedor 2, en función de si desea los resultados de las ventanas 1 o 2.

El identificador de contexto del reconocedor puede ser cualquier cosa que desee. Pero normalmente es un índice en una matriz global de estructuras. Las estructuras pueden contener todos los trazos que se han escrito y todas las variables que el reconocedor utiliza para esa parte de la tinta concreta (por ejemplo, la estructura Lattice interna o el estado actual de reconocimiento). Una estructura puede contener toda la información que el reconocedor necesita y utiliza para una parte determinada de la entrada de lápiz.

Para obtener un identificador de **HRECOCONTEXT** , llame a la función [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Observaciones

A continuación se enumeran las funciones de **HRECOCONTEXT**



| Función                                                            | Descripción                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Agrega un trazo de tinta al contexto del reconocedor.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Impide que el reconocedor procese la entrada manuscrita porque se está agregando o eliminando un nuevo trazo.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Crea un contexto de reconocedor que contiene la misma configuración que la original. El nuevo contexto de Reconocedor no incluye los resultados de la tinta o el reconocimiento del original.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indica que no se agregará más tinta al contexto.<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Devuelve una lista de alternativas para la mejor cadena de resultado.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Devuelve un puntero de [identificador de HRECOALT](hrecoalt-handle.md) para el mejor resultado alternativo.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Devuelve la mejor cadena de resultado.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Devuelve una lista de las propiedades que admite el reconocedor.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Devuelve un valor de propiedad especificado desde el contexto del reconocedor.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Devuelve una lista de los intervalos de puntos Unicode habilitados en el contexto.<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Devuelve la guía utilizada para la entrada con líneas o con conversión boxing.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Devuelve un puntero a la Lattice para los resultados actuales.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Devuelve un valor que indica si una palabra, una fecha, una hora, un número u otro texto que se pasa se incluye en el diccionario.<br/>                                                                                                               |
| [**Proceso**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Realiza el reconocimiento de tinta de forma sincrónica.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Elimina la entrada de lápiz actual y los resultados de reconocimiento del contexto.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Especifica el modo de autocompletar caracteres para el reconocimiento de caracteres o palabras.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Agrega una propiedad al contexto del reconocedor. Si ya existe una propiedad, se modifica su valor.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Habilita uno o más intervalos de puntos Unicode en el contexto.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Establece el Factoid que utiliza un reconocedor para restringir la búsqueda del resultado.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Establece cómo el reconocedor interpreta la tinta y determina la cadena de resultado.<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Establece la guía que se va a usar para la entrada con líneas o con conversión boxing.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Proporciona las cadenas de texto que aparecen antes y después del texto contenido en el contexto del reconocedor. En el caso de los reconocedores de caracteres de Asia oriental, la función [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) proporciona caracteres en lugar de cadenas de texto.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Establece la lista de palabras para que reconozca el contexto del reconocedor actual.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Resumen. h</dt> </dl> |



 

