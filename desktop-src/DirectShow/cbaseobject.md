---
description: La clase CBaseObject es una clase abstracta para implementar DirectShow objetos . Para implementar objetos del Modelo de objetos componentes (COM), use la clase CUnknown, que se deriva de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Clase CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261559"
---
# <a name="cbaseobject-class"></a>CBaseObject (clase)

La **clase CBaseObject** es una clase abstracta para implementar DirectShow objetos. Para implementar objetos del Modelo de objetos componentes (COM), use la [**clase CUnknown,**](cunknown.md) que se deriva de **CBaseObject**.



| Métodos de clase                                      | Descripción                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Método constructor.                    |
| [**~CBaseObject**](cbaseobject--cbaseobject.md)   | Método destructor.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Recupera el recuento de objetos activos. |



 

## <a name="remarks"></a>Observaciones

La mayoría de las DirectShow base derivan de **CBaseObject**. Esta clase proporciona asistencia para la depuración manteniendo un recuento de todos los objetos DirectShow activos durante el tiempo de ejecución. El recuento de objetos se almacena en una variable miembro estática de clase:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



En las compilaciones de depuración, el archivo DLL declara si se descarga mientras el número de objetos es mayor que cero. Esto facilita el seguimiento de las pérdidas causadas por problemas de recuento de referencias.

El **constructor CBaseObject** toma un argumento, un nombre de depuración para el objeto . Este nombre se almacena en una tabla global del archivo DLL. La [**función DbgDumpObjectRegister**](dbgdumpobjectregister.md) da formato a una lista de los objetos activos en el archivo DLL y la envía a la salida de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 




