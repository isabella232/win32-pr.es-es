---
description: El método GetEffect recupera el efecto en el nivel de prioridad especificado.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'IAMTimelineEffectable:: GetEffect (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681253"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>IAMTimelineEffectable:: GetEffect (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **GetEffect** recupera el efecto en el nivel de prioridad especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFX* \[ enuncia\]
</dt> <dd>

Recibe la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del efecto.

</dd> <dt>

*Cuales* 
</dt> <dd>

Nivel de prioridad del efecto que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HRESULT. Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                               | Descripción                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Ningún efecto con la prioridad especificada.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto.<br/>                             |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/>           |



 

## <a name="remarks"></a>Observaciones

Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




