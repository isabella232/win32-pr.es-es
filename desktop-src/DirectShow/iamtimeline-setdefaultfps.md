---
description: El método SetDefaultFPS establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo. Los grupos usan este valor como velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método IAMTimelineGroup::SetOutputFPS en el grupo.
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: Método IAMTimeline::SetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 20c352f40234672ceeb2d4c25ea9db04e89f712d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892241"
---
# <a name="iamtimelinesetdefaultfps-method"></a>IamTimeline::SetDefaultFPS (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetDefaultFPS` método establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo. Los grupos usan este valor como velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) en el grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FPS* 
</dt> <dd>

Velocidad de fotogramas predeterminada, en fotogramas por segundo.

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

 

 




