---
description: El \_ método de escalado Put especifica la cantidad por la que se ajusta verticalmente el borrado.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: 'IDxtJpeg: método de ut_ScaleY de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65a8b736dc66ec9dad20b1e261ecd7b0c4556774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679327"
---
# <a name="idxtjpegput_scaley-method"></a>IDxtJpeg::p \_ método de escalado UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_ScaleY` método especifica la cantidad por la que se ajusta verticalmente el borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Cantidad en la que se ajusta verticalmente el borrado, como porcentaje de la definición de borrador original. Por ejemplo, el valor 1,0 significa que no hay expansión y 2,0 significa que el 200% se ajusta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

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

[**Interfaz IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




