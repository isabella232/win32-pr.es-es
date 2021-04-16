---
description: El \_ método put MaskNum especifica el código de borrado de SMPTE del borrado.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'IDxtJpeg: método de ut_MaskNum de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679457"
---
# <a name="idxtjpegput_masknum-method"></a>IDxtJpeg::p \_ método MaskNum UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_MaskNum` método especifica el código de borrado de SMPTE del borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Especifica el código de borrado de SMPTE. Para obtener una lista de barridos SMPTE admitidos, consulte [transición de borrado de SMPTE](smpte-wipe-transition.md).

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

 

 




