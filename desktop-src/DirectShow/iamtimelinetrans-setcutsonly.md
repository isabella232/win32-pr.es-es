---
description: El método SetCutsOnly especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, puede que desee obtener una vista previa de la vista previa de la velocidad.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans:: SetCutsOnly (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691098"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>IAMTimelineTrans:: SetCutsOnly (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetCutsOnly` método especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, puede que desee obtener una vista previa de la vista previa de la velocidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Val* 
</dt> <dd>

Especifica si se va a representar la transición como un corte. Si es **true**, la transición se representa como un corte instantáneo. Si **es false**, la transición se representa a lo largo de su duración normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La representación de una transición como un corte no es compatible con el intercambio de las entradas. (Vea [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md)). Si se llama a `SetCutsOnly` con un valor de **true**, se invalida temporalmente el valor de **SetSwapInputs** . La configuración de solo cortes está pensada para la vista previa, sin embargo, por lo que esta limitación no afecta a la salida del archivo, simplemente Recuerde llamar a `SetCutsOnly` con el valor **false** antes de escribir el archivo.

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

[**Interfaz IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




