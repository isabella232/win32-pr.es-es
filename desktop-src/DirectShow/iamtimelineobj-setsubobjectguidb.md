---
description: 'El método SetSubObjectGUIDB especifica el GUID del subobjeto asociado a este objeto. Este método es equivalente a IAMTimelineObj:: SetSubObjectGUID, pero toma un valor BSTR.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'IAMTimelineObj:: SetSubObjectGUIDB (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679508"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a>IAMTimelineObj:: SetSubObjectGUIDB (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetSubObjectGUIDB` método especifica el GUID del subobjeto asociado a este objeto. Este método es equivalente a [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) , pero toma un valor **BSTR** .

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

**BSTR** que representa el GUID del subobjeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

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

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




