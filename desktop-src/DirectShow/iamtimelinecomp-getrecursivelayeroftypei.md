---
description: No compatible. En su lugar, llame al método IAMTimelineComp::GetRecursiveLayerOfType.
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: Método IAMTimelineComp::GetRecursiveLayerOfTypeI (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc62c0813aa38af450e2f5351390ec958dddd533cc203f52b3bfb70ff45344b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756425"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Método IAMTimelineComp::GetRecursiveLayerOfTypeI

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

No compatible. En su lugar, llame al método [**IAMTimelineComp::GetRecursiveLayerOfType.**](iamtimelinecomp-getrecursivelayeroftype.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVirtualTrack* 
</dt> <dd>

Reservado.

</dd> <dt>

*pWhichLayer* 
</dt> <dd>

Reservado.

</dd> <dt>

*Tipo* 
</dt> <dd>

Reservado.

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

[**IamTimelineComp (interfaz)**](iamtimelinecomp.md)
</dt> </dl>

 

 




