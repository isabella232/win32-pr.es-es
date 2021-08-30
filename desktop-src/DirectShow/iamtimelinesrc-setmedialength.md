---
description: El método SetMediaLength especifica la duración del archivo de origen.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: Método IAMTimelineSrc::SetMediaLength (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d2e4b608fea02ac8a7424e980ba3d3e63105e88bc0689d0ea281415bd14d00e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051665"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>IamTimelineSrc::SetMediaLength (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaLength` método especifica la duración del archivo de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Duración* 
</dt> <dd>

Longitud del medio, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Puede evitar posibles errores de representación estableciendo la longitud del medio antes de establecer el tiempo de detenerse del medio. Al establecer el tiempo de detenerse del medio, DES lo comprueba con respecto a la longitud del medio.

Este método no valida el *parámetro Length,* pero el valor debe ser igual a la duración real del archivo de origen. Obtenga la duración del archivo de origen llamando [**a IMediaDet::get \_ StreamLength.**](imediadet-get-streamlength.md)

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




