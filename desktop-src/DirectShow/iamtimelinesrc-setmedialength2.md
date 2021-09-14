---
description: El método SetMediaLength2 especifica la duración del archivo de origen. Este método es equivalente a IAMTimelineSrc::SetMediaLength, pero toma un valor REFTIME.
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: Método IAMTimelineSrc::SetMediaLength2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061087"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a>Método IAMTimelineSrc::SetMediaLength2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaLength2` método especifica la duración del archivo de origen. Este método es equivalente a [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), pero toma un [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Duración* 
</dt> <dd>

Longitud del medio, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




