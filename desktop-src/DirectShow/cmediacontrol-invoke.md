---
description: 'Método CMediaControl.Invoke: proporciona acceso a las propiedades y métodos expuestos por un objeto .'
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Método CMediaControl.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81f93b4ee22c12495b77c0a71b4a4602c7f93255446874e89a51678598ba8c67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655351"
---
# <a name="cmediacontrolinvoke-method"></a>Método CMediaControl.Invoke

Proporciona acceso a las propiedades y los métodos expuestos por un objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dispidMember* 
</dt> <dd>

Identificador del miembro. Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentación del objeto para obtener el identificador de distribución.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Debe ser IID \_ NULL.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretarán los argumentos.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la `CMediaControl::Invoke` llamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntero a una estructura que contiene una matriz de argumentos, una matriz de los IDs de distribución de argumentos para argumentos con nombre y recuentos del número de elementos de las matrices.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a donde se va a almacenar el resultado o **NULL** si el autor de la llamada no espera ningún resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntero a una estructura que contiene información de excepciones.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al índice del primer argumento, dentro de la matriz **rgvarg** de la estructura **DISLIGRAMS,** que tiene un error. Para obtener más información sobre **DIS DISRAMS,** consulte el SDK de plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve DISP \_ E \_ UNKNOWNINTERFACE si *riid* no es IID \_ NULL. Devuelve uno de los códigos de error de [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) si se produce un error en la llamada. De lo contrario, **devuelve el valor HRESULT** de la llamada a **IDispatch::Invoke**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaControl (clase)**](cmediacontrol.md)
</dt> </dl>

 

 




