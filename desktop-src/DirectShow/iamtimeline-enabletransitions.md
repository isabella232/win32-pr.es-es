---
description: El método EnableTransitions habilita o deshabilita todas las transiciones de la escala de tiempo.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: Método IAMTimeline::EnableTransitions (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266327"
---
# <a name="iamtimelineenabletransitions-method"></a>IamTimeline::EnableTransitions (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EnableTransitions` método habilita o deshabilita todas las transiciones de la escala de tiempo. Si las transiciones están deshabilitadas, los motores de representación las tratan como cortes; Es decir, la salida representada salta al instante de una pista a la siguiente. El punto de corte predeterminado se encuentra a la mitad de la duración de la transición. Puede cambiar el punto de corte llamando al [**método IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) en la transición. Las transiciones deshabilitadas no se quitan de la escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booleano que especifica si se deben habilitar o deshabilitar las transiciones. Si **es TRUE,** las transiciones están habilitadas. Si **es FALSE,** las transiciones están deshabilitadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




