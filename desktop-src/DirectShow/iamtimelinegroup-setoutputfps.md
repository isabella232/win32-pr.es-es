---
description: El método SetOutputFPS establece la velocidad de fotogramas de salida sin comprimir para este grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: Método IAMTimelineGroup::SetOutputFPS (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892073"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Método IAMTimelineGroup::SetOutputFPS

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

La salida representada de este grupo se ejecuta a la velocidad de fotogramas especificada y todas las ediciones del material de origen se redondean al límite de fotogramas más cercano, tal como se define en la velocidad de fotogramas. Para obtener el mejor rendimiento, use la misma velocidad de fotogramas para todos los grupos, vídeo y audio.

El [**método IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) sobrescribe la velocidad de fotogramas.

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

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




