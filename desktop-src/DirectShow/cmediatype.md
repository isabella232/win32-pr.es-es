---
description: La clase CMediaType administra los tipos de medios. Esta clase hereda la estructura \_ AM MEDIA \_ TYPE. Se puede convertir en una variable de tipo AM \_ MEDIA \_ TYPE.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: CMediaType (clase, Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49680848fc764cdbbdfeaf3bea363f29427a745297ef4fb39bca09159aa582f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831955"
---
# <a name="cmediatype-class"></a>CMediaType (clase)

![Jerarquía de clases cmediatype](images/mtype01.png)

La `CMediaType` clase administra los tipos de medios. Esta clase hereda la estructura [**\_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Se puede convertir en una variable de tipo **AM \_ MEDIA \_ TYPE**.



| Métodos públicos                                                      | Descripción                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Método constructor.                                                            |
| [**~CMediaType**](cmediatype--cmediatype.md)                       | Método destructor.                                                             |
| [**Establecer**](cmediatype-set.md)                                       | Establece el tipo de medio de otro tipo de medio.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Determina si se ha asignado un tipo principal a este objeto.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera el tipo principal.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Especifica el tipo principal.                                                      |
| [**Subtipo**](cmediatype-subtype.md)                               | Recupera el subtipo.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Especifica el subtipo.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina si las muestras tienen un tamaño fijo o un tamaño variable.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina si la secuencia usa compresión temporal.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Recupera el tamaño de la muestra.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Especifica un tamaño de muestra fijo o especifica que las muestras tienen un tamaño variable. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Especifica que las muestras no tienen un tamaño fijo.                               |
| [**SetComposiciónCompression**](cmediatype-settemporalcompression.md) | Especifica si las muestras se comprimen mediante compresión temporal.           |
| [**Formato**](cmediatype-format.md)                                 | Recupera un puntero al bloque de formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera la longitud del bloque de formato.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Especifica el tipo de formato.                                                     |
| [**Tipo de formato**](cmediatype-formattype.md)                         | Recupera el tipo de formato.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Especifica el bloque de formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Elimina el bloque de formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Asigna memoria para el bloque de formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Reallocates the format block to a new size.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inicializa el tipo de medio.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina si el tipo de medio está parcialmente definido.                             |
| Operadores                                                           | Descripción                                                                    |
| [**operator =**](cmediatype-operator-.md)                          | Sobrecarga el operador de asignación para copiar un tipo de medio.                        |
| [**operator ==**](cmediatype-operator--.md)                        | Comprueba la igualdad entre objetos `CMediaType`.                               |
| [**operador !=**](cmediatype-operator-neq.md)                      | Comprueba la desigualdad entre objetos `CMediaType`.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




