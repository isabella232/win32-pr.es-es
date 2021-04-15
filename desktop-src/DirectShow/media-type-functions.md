---
description: Las clases base de DirectShow proporcionan funciones auxiliares para controlar la \_ estructura de tipo de medio am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funciones de tipo de medio (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689930"
---
# <a name="media-type-functions"></a>Funciones de tipo de medio

Las clases base de DirectShow proporcionan funciones auxiliares para controlar la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

La estructura de **\_ \_ tipo de medio am** contiene un puntero (el miembro **pbFormat** ) a otro bloque de memoria, que se denomina *bloque de formato*. Al trabajar con esta estructura, por lo tanto, debe tener cuidado con la asignación de memoria para evitar pérdidas de memoria.

Las siguientes funciones asignan memoria:

-   **CreateMediaType** asigna una nueva estructura de **\_ \_ tipo de medio am** y el bloque de formato.
-   **CopyMediaType** copia en una estructura **de \_ \_ tipo de medio am** existente, pero asigna el bloque de formato.
-   **CreateAudioMediaType** Inicializa una estructura de **\_ \_ tipo de medio am** existente y, opcionalmente, asigna el bloque de formato.

Las siguientes funciones liberan memoria:

-   **FreeMediaType** libera el bloque de formato.
-   **DeleteMediaType** libera una estructura **de \_ \_ tipo de medio am** , incluido el bloque de formato.



| Función                                             | Descripción                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copia una estructura de **tipo de \_ medio \_ AM** asignada a tareas.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Inicializa una estructura de tipo de archivo multimedia a partir de una estructura de formato de onda.                                           |
| [**CreateMediaType**](createmediatype.md)           | Asigna e inicializa una estructura de **tipo de \_ medio \_ AM** a partir de una estructura de **\_ \_ tipo de medio am** existente. |
| [**DeleteMediaType**](deletemediatype.md)           | Elimina una estructura de **\_ \_ tipo de medio am** asignada por tarea.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libera una estructura de **\_ \_ tipo de medio am** asignada por tarea de la memoria.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




