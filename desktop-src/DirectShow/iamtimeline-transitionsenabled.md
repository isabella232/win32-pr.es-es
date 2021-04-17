---
description: El método TransitionsEnabled determina si las transiciones están habilitadas.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'IAMTimeline:: TransitionsEnabled (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690617"
---
# <a name="iamtimelinetransitionsenabled-method"></a>IAMTimeline:: TransitionsEnabled (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **TransitionsEnabled** determina si las transiciones están habilitadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Recibe un valor booleano. Si **es true**, las transiciones están habilitadas. De lo contrario, las transiciones están deshabilitadas.

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

[**Interfaz IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




