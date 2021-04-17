---
description: El método GetSwapInputs recupera un valor que indica si se intercambian las entradas de la transición.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'IAMTimelineTrans:: GetSwapInputs (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691024"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>IAMTimelineTrans:: GetSwapInputs (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetSwapInputs` método recupera un valor que indica si se intercambian las entradas de la transición.

De forma predeterminada, una transición va desde el compuesto de todas las capas de prioridad inferior hasta la capa en la que reside la transición. Puede invertir esta progresión, por lo que la transición va desde la capa en la que reside hasta el compuesto de capas de menor prioridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe un valor booleano. Si el valor es **false**, la transición va desde el compuesto de todas las capas de prioridad más baja hasta la capa de transición. Si el valor es **true**, la transición va en la dirección opuesta. El valor predeterminado es **FALSE**.

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

[**Interfaz IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




