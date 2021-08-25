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
ms.openlocfilehash: 2a6ab2205c1d86c747ffcabbe69a88de8898fa1315ec98f9b816a5f5983dee59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905255"
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

## <a name="remarks"></a>Comentarios

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

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




