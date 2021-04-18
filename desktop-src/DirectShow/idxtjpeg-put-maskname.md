---
description: El \_ método put MaskName especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: método de ut_MaskName de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680437"
---
# <a name="idxtjpegput_maskname-method"></a>IDxtJpeg::p \_ método MaskName UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_MaskName` método especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado. Esta máscara se usará en lugar de una de las máscaras de borrado integradas. El archivo debe contener un degradado monocromo de 8 bits por píxel. El degradado se usa como máscara para definir la progresión del barrido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Especifica el nombre del archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Para revertir a una máscara integrada, establezca la propiedad **MaskNum** .

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
</dt> <dt>

[**IDxtJpeg::p UT \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




