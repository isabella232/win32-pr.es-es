---
description: El método GetTimelineType recupera el tipo del objeto.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'IAMTimelineObj:: GetTimelineType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689933"
---
# <a name="iamtimelineobjgettimelinetype-method"></a>IAMTimelineObj:: GetTimelineType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetTimelineType` método recupera el tipo del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe un miembro del tipo enumerado de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo, que indica el tipo de objeto.

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

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




