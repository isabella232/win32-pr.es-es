---
description: Un identificador HRECOCONTEXT se usa para agregar entrada manuscrita al contexto, realizar el reconocimiento de entrada de lápiz (de forma sincrónica o asincrónica), recuperar el resultado del reconocimiento y recuperar alternativas.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Identificador HRECOCONTEXT (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267703"
---
# <a name="hrecocontext-handle"></a>Identificador HRECOCONTEXT

Un **identificador HRECOCONTEXT** se usa para agregar entrada manuscrita al contexto, realizar el reconocimiento de entrada de lápiz (de forma sincrónica o asincrónica), recuperar el resultado del reconocimiento y recuperar alternativas.

La razón principal para tener identificadores de contexto de reconocedor es diferenciar entre entradas de entrada de lápiz. Por ejemplo, puede crear una aplicación con dos ventanas, el usuario puede hacer entrada manuscrita en cualquiera de las ventanas. No desea que la entrada de lápiz de la primera ventana se mezcle con la entrada de lápiz de la segunda ventana cuando pida al reconocedor que reconozca la entrada de lápiz de una de las ventanas. En este tipo de aplicación, se crean dos contextos de reconocedor (uno para cada ventana) y se agregan trazos procedentes de la ventana 1 al contexto del reconocedor 1 y trazos de la ventana 2 al contexto del reconocedor 2. Para devolver los resultados del reconocimiento, llame al proceso en el contexto del reconocedor 1 o al contexto del reconocedor 2, en función de si desea que los resultados de la ventana 1 o 2.

El identificador de contexto del reconocedor puede ser cualquier cosa que desee. Pero normalmente es un índice de una matriz global de estructuras. Las estructuras pueden contener todos los trazos que se han escrito y todas las variables que el reconocedor usa para ese fragmento de lápiz determinado (por ejemplo, la estructura de celosía interna o el estado actual del reconocimiento). Una estructura puede contener toda la información que el reconocedor necesita y usa para un fragmento de lápiz determinado.

Para obtener un **identificador HRECOCONTEXT,** llame a la [**función CreateContext.**](/windows/desktop/api/recapis/nf-recapis-createcontext)


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Observaciones

Las siguientes son las **funciones DE HRECOCONTEXT**



| Función                                                            | Descripción                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Agrega un trazo de lápiz al contexto del reconocedor.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Impide que el reconocedor procese la entrada de lápiz porque se agrega o elimina un nuevo trazo.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Crea un contexto de reconocedor que contiene la misma configuración que el original. El nuevo contexto de reconocedor no incluye los resultados de reconocimiento ni de entrada de lápiz del original.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indica que no se agregará más entrada de lápiz al contexto.<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Devuelve una lista de alternativas para la mejor cadena de resultado.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Devuelve un [puntero HRECOALT Handle](hrecoalt-handle.md) para obtener el mejor resultado alternativo.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Devuelve la mejor cadena de resultado.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Devuelve una lista de propiedades que admite el reconocedor.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Devuelve un valor de propiedad especificado del contexto del reconocedor.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Devuelve una lista de intervalos de puntos Unicode habilitados en el contexto.<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Devuelve la guía que se usa para la entrada con formato boxeado o forrado.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Devuelve un puntero al lattice para los resultados actuales.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Devuelve un valor que indica si una palabra, fecha, hora, número u otro texto que se pasa está incluido en el diccionario.<br/>                                                                                                               |
| [**Proceso**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Realiza el reconocimiento de entrada de lápiz sincrónicamente.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Elimina los resultados actuales de la entrada de lápiz y el reconocimiento del contexto.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Especifica el modo autocompletar de caracteres para el reconocimiento de caracteres o palabras.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Agrega una propiedad al contexto del reconocedor. Si ya existe una propiedad, se modifica su valor.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Habilita uno o varios intervalos de puntos Unicode en el contexto.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Establece el factoid que usa un reconocedor para restringir la búsqueda del resultado.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Establece cómo el reconocedor interpreta la entrada de lápiz y determina la cadena de resultado.<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Establece la guía que se usará para la entrada con formato boxeado o forrado.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Proporciona las cadenas de texto que vienen antes y después del texto contenido en el contexto del reconocedor. Para los reconocedores de caracteres de Asia Oriental, la [**función SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) proporciona caracteres en lugar de cadenas de texto.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Establece la lista de palabras para el contexto del reconocedor actual que se reconocerá.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

