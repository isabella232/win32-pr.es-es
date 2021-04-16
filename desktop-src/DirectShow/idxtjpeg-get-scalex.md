---
description: El \_ método get scaleX recupera la cantidad por la que se ajusta horizontalmente el borrado.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Método IDxtJpeg:: get_ScaleX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680191"
---
# <a name="idxtjpegget_scalex-method"></a>IDxtJpeg:: get \_ scaleX (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_ScaleX` método recupera la cantidad por la que se ajusta horizontalmente el borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe la cantidad por la que se ajusta horizontalmente el borrado, como un porcentaje de la definición de borrado original. Por ejemplo, el valor 1,0 significa que no hay expansión y 2,0 significa que el 200% se ajusta.

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

 

 




