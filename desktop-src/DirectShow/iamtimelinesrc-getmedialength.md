---
description: El método GetMediaLength recupera la longitud del medio de este objeto de origen.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: Método IAMTimelineSrc::GetMediaLength (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72aeb68b3b3f9b31dc9ba00b2ffe8d82e2df8f8c5271abffcbd7737fa65203ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131185"
---
# <a name="iamtimelinesrcgetmedialength-method"></a>IamTimelineSrc::GetMediaLength (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetMediaLength` método recupera la longitud del medio de este objeto de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLength* 
</dt> <dd>

Recibe la longitud del medio en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                     | Descripción                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Correcto.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | Los tiempos de medios no se establecen en este objeto.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>       | **Argumento de** puntero NULL.<br/>              |



 

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




