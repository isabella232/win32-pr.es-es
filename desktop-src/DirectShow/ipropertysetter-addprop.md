---
description: El método AddProp agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter:: AddProp (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679121"
---
# <a name="ipropertysetteraddprop-method"></a>IPropertySetter:: AddProp (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `AddProp` método agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro* \[ de\]
</dt> <dd>

[**Dexterity \_**](dexter-param.md) Estructura de parámetro que especifica la propiedad. El miembro **nvalores** de la estructura debe ser igual al tamaño de la matriz proporcionada en el parámetro *pavalue* .

</dd> <dt>

*Pavalue* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) que contienen pares de valor de tiempo. La matriz debe estar en orden de tiempo ascendente. Las horas son relativas a la hora de inicio del efecto o de la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La primera estructura de [**\_ valor de Dexterity**](dexter-value.md) debe especificar una hora de referencia de cero y una marca de interpolación (**dwInterp**) de **DEXTERF \_ salto**, o el método devuelve un error.

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

 

 




