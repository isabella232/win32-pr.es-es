---
description: Proporciona acceso a las propiedades y los métodos expuestos por un objeto.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Método CMediaControl. Invoke (Ctlutil. h)
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
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680314"
---
# <a name="cmediacontrolinvoke-method"></a>CMediaControl. Invoke (método)

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

Identificador del miembro. Use [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentación del objeto para obtener el identificador de envío.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Debe ser un IID \_ null.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretan los argumentos.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la `CMediaControl::Invoke` llamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntero a una estructura que contiene una matriz de argumentos, una matriz de identificadores de envío de argumentos para argumentos con nombre y recuentos del número de elementos de las matrices.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero al lugar donde se va a almacenar el resultado o **null** si el llamador no espera ningún resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntero a una estructura que contiene la información de la excepción.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero al índice del primer argumento, dentro de la matriz **rgvarg** de la estructura **DISPPARAMS** , que tiene un error. Para obtener más información sobre **DISPPARAMS**, vea el SDK de la plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve DISP \_ E \_ UNKNOWNINTERFACE si *riid* no es \_ null. Devuelve uno de los códigos de error de [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) si se produce un error en la llamada. De lo contrario, devuelve el **HRESULT** de la llamada a **IDispatch:: Invoke**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




