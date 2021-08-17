---
description: El método EnableEffects habilita o deshabilita todos los efectos de la escala de tiempo. Si los efectos están deshabilitados, permanecen en la escala de tiempo, pero no se representan.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: Método IAMTimeline::EnableEffects (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a6cce5d06b65bb6a7b3b6063e6cf6b9190e268ba7ee5f5abadf4343be2cf64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401116"
---
# <a name="iamtimelineenableeffects-method"></a>Método IAMTimeline::EnableEffects

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EnableEffects` método habilita o deshabilita todos los efectos de la escala de tiempo. Si los efectos están deshabilitados, permanecen en la escala de tiempo, pero no se representan.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booleano que especifica si se deben habilitar o deshabilitar los efectos. Si **es TRUE,** los efectos están habilitados. Si **es FALSE,** los efectos están deshabilitados.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




