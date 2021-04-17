---
description: El método Remove quita este objeto de la escala de tiempo (incluidos los subobjetos pero no los elementos secundarios) para volver a insertarlo en otro lugar.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj:: Remove (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690729"
---
# <a name="iamtimelineobjremove-method"></a>IAMTimelineObj:: Remove (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `Remove` método quita este objeto de la escala de tiempo (incluidos los subobjetos pero no los elementos secundarios) para volver a insertar en cualquier lugar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Llame a este método solo si la aplicación volverá a insertar inmediatamente el objeto en la escala de tiempo. Se trata de una operación no válida para llamar a este método sin volver a insertar el objeto. Para quitar un objeto de forma permanente, llame a [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).

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

 

 




