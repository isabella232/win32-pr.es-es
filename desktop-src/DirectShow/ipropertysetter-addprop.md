---
description: El método AddProp agrega una propiedad al setter de propiedad, con una matriz de pares de tiempo-valor que definen el valor de la propiedad durante un intervalo de tiempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: Método IPropertySetter::AddProp (Qedit.h)
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
ms.openlocfilehash: b2a4cf2f730d177b4eb9323e882d5030c6fc1d658ede574e74d9d222e81d677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818614"
---
# <a name="ipropertysetteraddprop-method"></a>IPropertySetter::AddProp (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método agrega una propiedad al setter de propiedad, con una matriz de pares de tiempo-valor que definen el valor de la propiedad `AddProp` durante un intervalo de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param* \[ En\]
</dt> <dd>

[**ASÍNstro \_ Estructura PARAM**](dexter-param.md) que especifica la propiedad . El **miembro nValues** de la estructura debe ser igual al tamaño de la matriz especificada en el *parámetro paValue.*

</dd> <dt>

*paValue* \[ En\]
</dt> <dd>

Puntero a una matriz de [**estructuras VALUE DE COLOR \_ QUE**](dexter-value.md) contienen pares de tiempo-valor. La matriz debe estar en orden de hora ascendente. Las horas son relativas a la hora de inicio del efecto o la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La primera [**estructura DE \_ VALOR DE LA**](dexter-value.md) PROPIEDAD debe especificar un tiempo de referencia de cero y una marca de interpolación (**dwInterp**) de JUMP **de \_ LAFF,** o bien el método devuelve un error.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




