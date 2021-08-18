---
description: El método TrackGetPriority recupera el nivel de prioridad del objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: Método IAMTimelineVirtualTrack::TrackGetPriority (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 10d84e3427cb13006cb3e674867dddb344f19a851d2afae09ad848b268e48dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051995"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a>IamTimelineVirtualTrack::TrackGetPriority (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `TrackGetPriority` método recupera el nivel de prioridad del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPriority* 
</dt> <dd>

Puntero a una variable que recibe el nivel de prioridad. Si el objeto no forma parte de una escala de tiempo, el valor se establece en –1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineVirtualTrack (interfaz)**](iamtimelinevirtualtrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




