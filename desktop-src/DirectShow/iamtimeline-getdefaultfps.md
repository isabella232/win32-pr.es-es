---
description: 'El método GetDefaultFPS recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo (FPS). Los grupos usan este valor como la velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método IAMTimelineGroup:: SetOutputFPS en el grupo.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'IAMTimeline:: GetDefaultFPS (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679476"
---
# <a name="iamtimelinegetdefaultfps-method"></a>IAMTimeline:: GetDefaultFPS (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetDefaultFPS` método recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo (FPS). Los grupos usan este valor como la velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) en el grupo.

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

 

 




