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
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892169"
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

[**IamTimelineComp (interfaz)**](iamtimelinecomp.md)
</dt> </dl>

 

 




