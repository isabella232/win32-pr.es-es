---
description: El método GetRecursiveLayerOfType realiza una ordenación en profundidad de las pistas virtuales contenidas en esta composición y recupera la enésima pista virtual de esa ordenación.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: Método IAMTimelineComp::GetRecursiveLayerOfType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892164"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>IamTimelineComp::GetRecursiveLayerOfType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método realiza una ordenación en profundidad de las pistas virtuales contenidas en esta composición y recupera la enésima pista `GetRecursiveLayerOfType` virtual de esa ordenación. 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVirtualTrack* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*WhichLayer* 
</dt> <dd>

Especifica la pista virtual que se va a recuperar, indexada desde cero.

</dd> <dt>

*Tipo* 
</dt> <dd>

Miembro del tipo [**enumerado TIMELINE \_ MAJOR \_ TYPE**](timeline-major-type.md) que especifica si se deben incluir pistas en la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ningún objeto del tipo especificado.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>       |



 

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación no necesitará llamar a este método.

Si el *parámetro Type* es TIMELINE MAJOR \_ TYPE \_ \_ TRACK, el orden de profundidad incluye pistas. Si no es así, solo incluye composiciones y grupos. El propio objeto se incluye en la ordenación.

Por ejemplo, en la siguiente disposición, a partir de la composición A, el orden sería B, C, F, D, E, A.

![getrecursivelayeroftype](images/composition.png)

Si el método se realiza correctamente, la **interfaz IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimelineComp (Interfaz)**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




