---
description: El método SetSwapInputs especifica si se intercambian las entradas de la transición.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'IAMTimelineTrans:: SetSwapInputs (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690918"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>IAMTimelineTrans:: SetSwapInputs (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetSwapInputs` método especifica si se intercambian las entradas de la transición.

De forma predeterminada, una transición va desde el compuesto de todas las capas de prioridad inferior hasta la capa en la que reside la transición. Puede invertir esta progresión, por lo que la transición va desde la capa en la que reside hasta el compuesto de capas de menor prioridad. Para obtener más información, consulte dirección de la [transición](transition-direction.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Val* 
</dt> <dd>

Especifica si se intercambian las entradas. Si **es false**, la transición va del compuesto de todas las capas de prioridad inferior a la capa de transición. Si **es true**, la transición va en la dirección opuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método no cambia la dirección del efecto visual. Por ejemplo, un borrado de izquierda a derecha seguirá desplazando de izquierda a derecha. Para cambiar la dirección, establezca la propiedad **Progress** mediante la interfaz [**IPropertySetter**](ipropertysetter.md) .

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

[**Interfaz IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




