---
description: El \_ método get Filter recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Método IMediaDet:: get_Filter (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680896"
---
# <a name="imediadetget_filter-method"></a>IMediaDet:: get ( \_ método de filtro)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_Filter` método recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Recibe un puntero a la interfaz **IUnknown** del filtro. Si no hay ningún filtro de origen en uso, el valor se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando el método devuelve un valor, si *\* ppVal* no es **null**, la interfaz **IUnknown** tiene un recuento de referencias pendiente. Suelte la interfaz cuando termine de usarla.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




