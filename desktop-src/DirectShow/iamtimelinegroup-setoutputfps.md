---
description: El método SetOutputFPS establece la velocidad de fotogramas de salida sin comprimir para este grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'IAMTimelineGroup:: SetOutputFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690790"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>IAMTimelineGroup:: SetOutputFPS (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetOutputFPS` método establece la velocidad de fotogramas de salida sin comprimir para este grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FPS* 
</dt> <dd>

Velocidad de fotogramas de salida para este grupo, en fotogramas por segundo. El valor no puede ser igual a cero y no puede tener más de siete dígitos después de la posición decimal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La salida representada de este grupo se ejecuta a la velocidad de fotogramas especificada y todas las ediciones del material de origen se redondean al límite de fotogramas más cercano, según se define en la velocidad de fotogramas. Para obtener el mejor rendimiento, use la misma velocidad de fotogramas para todos los grupos, vídeo y audio.

El método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) sobrescribe la velocidad de fotogramas.

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

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




