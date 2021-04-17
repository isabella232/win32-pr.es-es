---
description: La clase CMediaType administra los tipos de medios. Esta clase hereda la estructura de \_ tipo de medio am \_ . Se puede convertir en una variable de tipo AM \_ media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Clase CMediaType (mtype. h)
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
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670760"
---
# <a name="cmediatype-class"></a>Clase CMediaType

![jerarquía de clases cmediatype](images/mtype01.png)

La `CMediaType` clase administra los tipos de medios. Esta clase hereda la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Se puede convertir en una variable de tipo **AM \_ media \_ Type**.



| Métodos públicos                                                      | Descripción                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Método de constructor.                                                            |
| [**~ CMediaType**](cmediatype--cmediatype.md)                       | Método de destructor.                                                             |
| [**Conjunto**](cmediatype-set.md)                                       | Establece el tipo de medio desde otro tipo de medio.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Determina si se ha asignado un tipo principal a este objeto.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera el tipo principal.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Especifica el tipo principal.                                                      |
| [**Subtype**](cmediatype-subtype.md)                               | Recupera el subtipo.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Especifica el subtipo.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina si los ejemplos tienen un tamaño fijo o un tamaño variable.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina si la secuencia utiliza la compresión temporal.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Recupera el tamaño de la muestra.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Especifica que los ejemplos no tienen un tamaño fijo.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Especifica si los ejemplos se comprimen mediante la compresión temporal.           |
| [**Aplique**](cmediatype-format.md)                                 | Recupera un puntero al bloque de formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera la longitud del bloque de formato.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Especifica el tipo de formato.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Recupera el tipo de formato.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Especifica el bloque de formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Elimina el bloque de formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Asigna memoria para el bloque de formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Reasigna el bloque de formato a un nuevo tamaño.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inicializa el tipo de archivo multimedia.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina si el tipo de medio se define parcialmente.                             |
| Operadores                                                           | Descripción                                                                    |
| [**operador =**](cmediatype-operator-.md)                          | Sobrecarga el operador de asignación para copiar un tipo de archivo multimedia.                        |
| [**operador = =**](cmediatype-operator--.md)                        | Comprueba la igualdad entre objetos `CMediaType`.                               |
| [**operador! =**](cmediatype-operator-neq.md)                      | Comprueba la desigualdad entre objetos `CMediaType`.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




