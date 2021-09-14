---
description: El método SetDefaultTransitionB establece la transición predeterminada. Este método es equivalente a IAMTimeline::SetDefaultTransition, pero toma un valor BSTR, en lugar de un puntero a un GUID.
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: Método IAMTimeline::SetDefaultTransitionB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 221491dd0be97f1808e469d956c189bf61458278
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892236"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a>IamTimeline::SetDefaultTransitionB (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetDefaultTransitionB` método establece la transición predeterminada. Este método es equivalente a [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md), pero toma un valor BSTR, en lugar de un puntero a un GUID.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Valor BSTR que representa el GUID de la transición predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

 

 




