---
description: El método GetVTrack recupera la pista virtual con la prioridad especificada.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: Método IAMTimelineComp::GetVTrack (Qedit.h)
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
ms.openlocfilehash: 245f19783f7a472f86544d14f27c588e7a5938e899f2f389887d7a7817d6254e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756305"
---
# <a name="iamtimelinecompgetvtrack-method"></a>IamTimelineComp::GetVTrack (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

*ppVirtualTrack* \[ out\]
</dt> <dd>

Recibe la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*Que* 
</dt> <dd>

Prioridad de la pista virtual que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ninguna pista virtual con la prioridad especificada.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>                    |



 

## <a name="remarks"></a>Comentarios

Si el método se realiza correctamente, la **interfaz IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineComp (Interfaz)**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




