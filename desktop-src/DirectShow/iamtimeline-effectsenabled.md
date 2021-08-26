---
description: El método EffectsEnabled determina si los efectos están habilitados. Si los efectos están deshabilitados, permanecen en la escala de tiempo, pero no se representan.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: Método IAMTimeline::EffectsEnabled (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e63561c62f3cbaf7a3a257179167e657ee4d10c6206b6d74062039362b272aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905285"
---
# <a name="iamtimelineeffectsenabled-method"></a>IamTimeline::EffectsEnabled (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EffectsEnabled` método determina si los efectos están habilitados. Si los efectos están deshabilitados, permanecen en la escala de tiempo, pero no se representan.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Recibe un valor booleano que indica si los efectos están habilitados. Si **es TRUE,** los efectos están habilitados. Si **es FALSE,** los efectos están deshabilitados.

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

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




