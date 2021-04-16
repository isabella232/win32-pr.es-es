---
description: El \_ método put size establece el tamaño de salida y el modo de ajuste.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: método de ut_Size de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679439"
---
# <a name="iresizeput_size-method"></a>IResize: método de tamaño de:p UT \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_Size` método establece el tamaño de salida y el modo de ajuste.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alto* \[ de de\]
</dt> <dd>

Alto del vídeo, en píxeles.

</dd> <dt>

*Ancho* \[ de de\]
</dt> <dd>

Ancho del vídeo, en píxeles.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Modo de ajuste. Vea [**cambiar el tamaño**](resize-flags.md) de las marcas para los valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

DES puede llamar a este método antes o después de llamar a **Put \_ mediatype**. Si DES llama a este método antes de llamar a **Put \_ mediatype**, el filtro debe seleccionar un valor predeterminado para la profundidad de bits y usar los valores de tamaño para construir un tipo de medio de salida. Si DES llama a este método después de llamar a **Put \_ mediatype**, el filtro debe modificar su tipo de salida actual con los nuevos tamaños.

DES también puede llamar a este método después de que el PIN de salida esté conectado. En ese caso, modifique el tipo de salida y vuelva a conectar el PIN de salida con el nuevo tipo. Consulte [reconexión de PIN](reconnecting-pins.md) para obtener más información.

El parámetro *Flags* especifica cómo el filtro debe realizar la operación de cambio de tamaño.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9,0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IResize**](iresize.md)
</dt> </dl>

 

 




