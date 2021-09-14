---
description: El método GetDefaultFPS recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo (FPS). Los grupos usan este valor como velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método IAMTimelineGroup::SetOutputFPS en el grupo.
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: Método IAMTimeline::GetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062324"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Método IAMTimeline::GetDefaultFPS

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetDefaultFPS` método recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo (FPS). Los grupos usan este valor como velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) en el grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFPS* 
</dt> <dd>

Recibe la velocidad de fotogramas predeterminada, en fotogramas por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




