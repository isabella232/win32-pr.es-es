---
description: El método FreeProps libera los recursos asignados por el método IPropertySetter::GetProps. Llame a este método después de llamar a GetProps y pasarle las estructuras devueltas por GetProps.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: Método IPropertySetter::FreeProps (Qedit.h)
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
ms.openlocfilehash: 34529c7d78ad36a87eb441f624af8daf1167a77148758ff376feacc70250f18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397556"
---
# <a name="ipropertysetterfreeprops-method"></a>IPropertySetter::FreeProps (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `FreeProps` método libera los recursos asignados por el método [**IPropertySetter::GetProps.**](ipropertysetter-getprops.md) Llame a este método después de llamar **a GetProps** y pasarle las estructuras **devueltas por GetProps.**

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

*cParams* \[ En\]
</dt> <dd>

Número de elementos de la matriz *paParam.*

</dd> <dt>

*paParam* \[ En\]
</dt> <dd>

Puntero a una matriz de [**estructuras DE PARAM DE TIPO \_ ASÍN.**](dexter-param.md)

</dd> <dt>

*paValue* \[ En\]
</dt> <dd>

Puntero a una matriz de [**estructuras VALUE DE TIPO \_ ASÍN.**](dexter-value.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




