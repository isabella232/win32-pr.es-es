---
description: El método SetCutsOnly especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, es posible que desee obtener una vista previa como un corte para acelerar la vista previa.
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
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154744"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>IamTimelineTrans::SetCutsOnly (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetCutsOnly` método especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, es posible que desee obtener una vista previa como un corte para acelerar la vista previa.

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

## <a name="remarks"></a>Comentarios

La representación de una transición como un corte no es compatible con el intercambio de las entradas. (Vea [**IAMTimelineTrans::SetSwapInputs).**](iamtimelinetrans-setswapinputs.md) Si llama `SetCutsOnly` a con un valor **true**, invalida temporalmente la configuración **SetSwapInputs.** Sin embargo, la configuración de solo cortes está pensada para la versión preliminar, por lo que esta limitación no afecta a la salida del archivo, simplemente recuerde llamar a con el valor FALSE antes de `SetCutsOnly` escribir el archivo. 

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

[**IamTimelineTrans (interfaz)**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




