---
description: El método GetDefaultTransitionB recupera la transición predeterminada. Este método es equivalente a IAMTimeline::GetDefaultTransition, pero recibe un valor BSTR, en lugar de un GUID.
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: Método IAMTimeline::GetDefaultTransitionB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062319"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a>IamTimeline::GetDefaultTransitionB (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetDefaultTransitionB` método recupera la transición predeterminada. Este método es equivalente a [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), pero recibe un valor BSTR, en lugar de un GUID.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Recibe un **valor BSTR** que representa el GUID de la transición predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El método asigna memoria para la cadena. La aplicación debe llamar **a SysFreeString para** liberar la memoria.

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

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




