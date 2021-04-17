---
description: El método SetOutputBuffering especifica el número de fotogramas representados de antemano durante la vista previa.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup:: SetOutputBuffering (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690791"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>IAMTimelineGroup:: SetOutputBuffering (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetOutputBuffering` método especifica el número de fotogramas representados de antemano durante la vista previa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nBuffer* \[ de\]
</dt> <dd>

Número de fotogramas que se almacenarán en búfer durante la vista previa. Debe ser dos o más.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Un búfer mayor requiere más memoria, pero puede dar lugar a una vista previa más suave, especialmente durante los efectos o las transiciones que requieren más tiempo para representarse. El búfer predeterminado es 30 fotogramas.

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

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




