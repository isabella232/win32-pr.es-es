---
description: 'El método SetMediaLength2 especifica la duración del archivo de código fuente. Este método es equivalente a IAMTimelineSrc:: SetMediaLength, pero toma un valor REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'IAMTimelineSrc:: SetMediaLength2 (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680570"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a>IAMTimelineSrc:: SetMediaLength2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetMediaLength2` método especifica la duración del archivo de código fuente. Este método es equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), pero toma un valor [**REFTIME**](reftime.md) .

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

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




