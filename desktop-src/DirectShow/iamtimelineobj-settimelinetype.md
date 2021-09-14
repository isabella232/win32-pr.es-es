---
description: No compatible. Llame al método IAMTimeline::CreateEmptyNode para crear un nuevo objeto de escala de tiempo. Una vez creado un objeto, no se puede cambiar su tipo.
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: Método IAMTimelineObj::SetTimelineType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061639"
---
# <a name="iamtimelineobjsettimelinetype-method"></a>IamTimelineObj::SetTimelineType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

No compatible. Llame al [**método IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) para crear un nuevo objeto de escala de tiempo. Una vez creado un objeto, no se puede cambiar su tipo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
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

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> </dl>

 

 




