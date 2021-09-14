---
description: El método GetDefaultEffectB recupera el efecto predeterminado. Este método es equivalente a IAMTimeline::GetDefaultEffect, pero recibe un valor BSTR en lugar de un GUID.
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: Método IAMTimeline::GetDefaultEffectB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062329"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>IamTimeline::GetDefaultEffectB (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetDefaultEffectB` método recupera el efecto predeterminado. Este método es equivalente a [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), pero recibe un **valor BSTR** en lugar de un GUID.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Recibe un **valor BSTR** que representa el GUID del efecto predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El método asigna memoria para la cadena. La aplicación debe llamar **a SysFreeString para** liberar la memoria.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




