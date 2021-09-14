---
description: El método SetCutsOnly especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, es posible que desee obtener una vista previa de ella como un corte para acelerar la vista previa.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: Método IAMTimelineTrans::SetCutsOnly (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072197"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Método IAMTimelineTrans::SetCutsOnly

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetCutsOnly` método especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, es posible que desee obtener una vista previa de ella como un corte para acelerar la vista previa.

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

Especifica si se va a representar la transición como un corte. Si **es TRUE,** la transición se representa como un corte instantáneo. Si **es FALSE,** la transición se representa durante su duración normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

La representación de una transición como un corte no es compatible con el intercambio de las entradas. (Vea [**IAMTimelineTrans::SetSwapInputs).**](iamtimelinetrans-setswapinputs.md) Si llama a `SetCutsOnly` con un valor **true**, invalida temporalmente la configuración **SetSwapInputs.** Sin embargo, la configuración de solo cortes está pensada para la versión preliminar, por lo que esta limitación no afecta a la salida del archivo, simplemente recuerde llamar a con el valor FALSE antes de `SetCutsOnly` escribir el archivo. 

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

[**IamTimelineTrans (interfaz)**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




