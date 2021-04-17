---
description: El método SrcAdd agrega un origen a la pista.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack:: SrcAdd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690112"
---
# <a name="iamtimelinetracksrcadd-method"></a>IAMTimelineTrack:: SrcAdd (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SrcAdd` método agrega un origen a la pista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. Devuelve E \_ nointerface si el objeto no es un objeto de origen. De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Establezca las horas de inicio y detención del origen antes de llamar a este método. (Llame a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md)).

Actualmente, DES no puede representar simultáneamente más de 75 orígenes que se comprimieron con códecs de administrador de compresión de vídeo (VCM). Además, si el proyecto como un conjunto contiene más de 75 tales orígenes, debe usar reconexión dinámica o DES no puede obtener una vista previa del proyecto. Para obtener más información, vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**Interfaz IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




