---
description: El método EnableTransitions habilita o deshabilita todas las transiciones de la escala de tiempo.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline:: EnableTransitions (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653515"
---
# <a name="iamtimelineenabletransitions-method"></a>IAMTimeline:: EnableTransitions (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `EnableTransitions` método habilita o deshabilita todas las transiciones de la escala de tiempo. Si se deshabilitan las transiciones, los motores de representación los tratan como cortes; es decir, la salida representada salta de forma instantánea de una pista a la siguiente. El punto de corte predeterminado está a mitad de la duración de la transición. Puede cambiar el punto de corte llamando al método [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) en la transición. Las transiciones deshabilitadas no se quitan de la escala de tiempo.

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

Valor booleano que especifica si se van a habilitar o deshabilitar las transiciones. Si **es true**, las transiciones están habilitadas. Si **es false**, las transiciones están deshabilitadas.

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

[**Interfaz IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




