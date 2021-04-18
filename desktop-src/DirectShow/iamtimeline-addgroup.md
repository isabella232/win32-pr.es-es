---
description: El método AddGroup agrega un grupo a la escala de tiempo.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'IAMTimeline:: AddGroup (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679387"
---
# <a name="iamtimelineaddgroup-method"></a>IAMTimeline:: AddGroup (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `AddGroup` método agrega un grupo a la escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGroup* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del grupo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                   | Descripción                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se ha superado el número máximo de grupos.<br/> |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | El objeto no es un grupo.<br/>         |



 

## <a name="remarks"></a>Observaciones

Actualmente, las escalas de tiempo admiten un máximo de 32 grupos.

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

 

 




