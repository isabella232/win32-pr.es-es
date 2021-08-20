---
description: Las DirectShow base proporcionan funciones auxiliares para controlar la estructura \_ AM MEDIA \_ TYPE.
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funciones de tipo de medio (Mtype.h)
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
ms.openlocfilehash: ef47b944d5d445f57779f99cb8517a773a7efba19ae3f2133f896fcba7b86548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153163"
---
# <a name="media-type-functions"></a>Funciones de tipo de medio

Las DirectShow base proporcionan funciones auxiliares para controlar la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

La **estructura AM MEDIA \_ \_ TYPE** contiene un puntero (el **miembro pbFormat)** a otro bloque de memoria, denominado bloque *de formato*. Al trabajar con esta estructura, por lo tanto, debe tener cuidado con la asignación de memoria para evitar pérdidas de memoria.

Las siguientes funciones asignan memoria:

-   **CreateMediaType asigna** una nueva estructura **AM MEDIA \_ \_ TYPE** y el bloque de formato.
-   **CopyMediaType copia** en una estructura **DE AM MEDIA \_ \_ TYPE** existente, pero asigna el bloque de formato.
-   **CreateAudioMediaType** inicializa una estructura **DE AM MEDIA \_ \_ TYPE** existente y, opcionalmente, asigna el bloque de formato.

Las siguientes funciones liberan memoria:

-   **FreeMediaType libera** el bloque de formato.
-   **DeleteMediaType libera** una estructura **AM MEDIA \_ \_ TYPE,** incluido el bloque de formato.



| Función                                             | Descripción                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copia una estructura AM **\_ MEDIA TYPE \_ asignada** por tarea.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Inicializa una estructura de tipo de medio dada una estructura de formato de onda.                                           |
| [**CreateMediaType**](createmediatype.md)           | Asigna e inicializa una estructura **AM \_ MEDIA \_ TYPE,** a partir de una estructura **DE AM MEDIA \_ \_ TYPE** existente. |
| [**DeleteMediaType**](deletemediatype.md)           | Elimina una estructura AM **\_ MEDIA \_ TYPE** asignada por tarea.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libera una estructura AM **\_ MEDIA \_ TYPE** asignada por tarea de la memoria.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




