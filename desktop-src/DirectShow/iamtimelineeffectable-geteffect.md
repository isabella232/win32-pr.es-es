---
description: El método GetEffect recupera el efecto en el nivel de prioridad especificado.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: Método IAMTimelineEffectable::GetEffect (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887044"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>IamTimelineEffectable::GetEffect (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método GetEffect** recupera el efecto en el nivel de prioridad especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFX* \[ out\]
</dt> <dd>

Recibe la interfaz [**IAMTimelineObj del**](iamtimelineobj.md) efecto.

</dd> <dt>

*Que* 
</dt> <dd>

Nivel de prioridad del efecto que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HRESULT. Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                               | Descripción                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Ningún efecto en la prioridad especificada,<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/>           |



 

## <a name="remarks"></a>Observaciones

Si el método devuelve S \_ OK, la **interfaz IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IAMTimelineEffectable (Interfaz)**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




