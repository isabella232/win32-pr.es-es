---
description: El método SetStretchMode establece el modo stretch. El modo de ajuste determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: Método IAMTimelineSrc::SetStretchMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891916"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>IamTimelineSrc::SetStretchMode (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetStretchMode` método establece el modo de ajuste. El modo de ajuste determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Marca que indica el modo de ajuste actual. Para obtener una lista de valores posibles, vea [**Cambiar el tamaño de las marcas**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




