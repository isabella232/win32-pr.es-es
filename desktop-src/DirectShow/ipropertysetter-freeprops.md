---
description: 'El método FreeProps libera los recursos asignados por el método IPropertySetter:: GetProps. Llame a este método después de llamar a GetProps, pasándole las estructuras devueltas por GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter:: FreeProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679119"
---
# <a name="ipropertysetterfreeprops-method"></a>IPropertySetter:: FreeProps (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `FreeProps` método libera los recursos asignados por el método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) . Llame a este método después de llamar a **GetProps**, pasándole las estructuras devueltas por **GetProps**.

## <a name="syntax"></a>Sintaxis


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cParams* \[ de\]
</dt> <dd>

Número de elementos de la matriz de *paparam* .

</dd> <dt>

*param* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras de [**\_ parámetros de Dexterity**](dexter-param.md) .

</dd> <dt>

*Pavalue* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

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

[**Interfaz IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




