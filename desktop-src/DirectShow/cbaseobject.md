---
description: La clase CBaseObject es una clase abstracta para implementar objetos de DirectShow. Para implementar objetos del modelo de objetos componentes (COM), use la clase CUnknown, que se deriva de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Clase CBaseObject (ComBase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670668"
---
# <a name="cbaseobject-class"></a>Clase CBaseObject

La clase **CBaseObject** es una clase abstracta para implementar objetos de DirectShow. Para implementar objetos del modelo de objetos componentes (COM), use la clase [**CUnknown**](cunknown.md) , que se deriva de **CBaseObject**.



| Métodos de clase                                      | Descripción                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Método de constructor.                    |
| [**~ CBaseObject**](cbaseobject--cbaseobject.md)   | Método de destructor.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Recupera el recuento de objetos activos. |



 

## <a name="remarks"></a>Observaciones

La mayoría de las clases base de DirectShow derivan de **CBaseObject**. Esta clase proporciona ayuda para la depuración manteniendo un recuento de todos los objetos de DirectShow activos durante el tiempo de ejecución. El recuento de objetos se almacena en una variable miembro de clase estática:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



En las compilaciones de depuración, el archivo DLL validará si se descarga mientras el recuento de objetos es mayor que cero. Esto facilita el seguimiento de las fugas producidas por problemas de recuento de referencias.

El constructor **CBaseObject** toma un argumento, un nombre de depuración para el objeto. Este nombre se almacena en una tabla global en el archivo DLL. La función [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) da formato a una lista de los objetos activos en el archivo dll y lo envía a la salida de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




