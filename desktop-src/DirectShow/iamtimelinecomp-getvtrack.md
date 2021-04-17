---
description: El método GetVTrack recupera la pista virtual con la prioridad especificada.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp:: GetVTrack (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680971"
---
# <a name="iamtimelinecompgetvtrack-method"></a>IAMTimelineComp:: GetVTrack (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetVTrack` método recupera la pista virtual con la prioridad especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVirtualTrack* \[ enuncia\]
</dt> <dd>

Recibe la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*Cuales* 
</dt> <dd>

Prioridad de la pista virtual que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                  | Descripción                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No hay ninguna pista virtual con la prioridad especificada.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/>                    |



 

## <a name="remarks"></a>Observaciones

Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




