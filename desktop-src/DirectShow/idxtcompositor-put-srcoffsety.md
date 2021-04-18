---
description: El \_ método put SrcOffsetY especifica el desplazamiento vertical del rectángulo de origen.
ms.assetid: abdc520f-8de6-4a4f-aa8f-facedaa8fce1
title: 'IDxtCompositor: método de ut_SrcOffsetY de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad574939ce9f3d694944d39af76787dd19a22735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679235"
---
# <a name="idxtcompositorput_srcoffsety-method"></a>IDxtCompositor::p \_ método SrcOffsetY UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_SrcOffsetY` método especifica el desplazamiento vertical del rectángulo de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_SrcOffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Desplazamiento vertical del rectángulo de origen, en píxeles.

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

[**Interfaz IDxtCompositor**](idxtcompositor.md)
</dt> </dl>

 

 




