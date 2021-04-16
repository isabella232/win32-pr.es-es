---
description: El método EnableEffects habilita o deshabilita todos los efectos de la escala de tiempo. Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'IAMTimeline:: EnableEffects (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679384"
---
# <a name="iamtimelineenableeffects-method"></a>IAMTimeline:: EnableEffects (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `EnableEffects` método habilita o deshabilita todos los efectos de la escala de tiempo. Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booleano que especifica si se deben habilitar o deshabilitar los efectos. Si **es true**, se habilitan los efectos. Si **es false**, los efectos están deshabilitados.

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

[**Interfaz IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




