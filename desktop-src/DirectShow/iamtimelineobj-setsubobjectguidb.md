---
description: El método SetSubObjectGUIDB especifica el GUID del subobjeto asociado a este objeto. Este método es equivalente a IAMTimelineObj::SetSubObjectGUID, pero toma un valor BSTR.
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: Método IAMTimelineObj::SetSubObjectGUIDB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061640"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a>Método IAMTimelineObj::SetSubObjectGUIDB

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetSubObjectGUIDB` método especifica el GUID del subobjeto asociado a este objeto . Este método es equivalente a [**IAMTimelineObj::SetSubObjectGUID,**](iamtimelineobj-setsubobjectguid.md) pero toma un **valor BSTR.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

**BSTR que** representa el GUID del subobjeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

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
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




