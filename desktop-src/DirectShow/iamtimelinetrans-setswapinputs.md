---
description: El método SetSwapInputs especifica si se intercambian las entradas de transición.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: Método IAMTimelineTrans::SetSwapInputs (Qedit.h)
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
ms.openlocfilehash: 3da350c6fe34f671d7af53ca67c404b4e327690918434b5e2fb1426e4a0953ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052085"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Método IAMTimelineTrans::SetSwapInputs

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetSwapInputs` método especifica si se intercambian las entradas de transición.

De forma predeterminada, una transición pasa de la composición de todas las capas de prioridad inferior a la capa donde reside la transición. Puede invertir esta progresión, por lo que la transición pasa de la capa donde reside de nuevo a la composición de capas de prioridad inferior. Para obtener más información, vea [Dirección de transición](transition-direction.md).

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

Especifica si se intercambian las entradas. Si **es FALSE,** la transición pasa de la composición de todas las capas de prioridad inferior a la capa de transición. Si **es TRUE,** la transición va en la dirección opuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método no cambia la dirección del efecto visual. Por ejemplo, un borrado de izquierda a derecha seguirá siendo de izquierda a derecha. Para cambiar la dirección, establezca la **propiedad Progress** mediante la [**interfaz IPropertySetter.**](ipropertysetter.md)

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineTrans (interfaz)**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




