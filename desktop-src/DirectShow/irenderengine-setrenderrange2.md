---
description: 'El método SetRenderRange2 establece el intervalo de tiempo en la escala de tiempo que se va a representar. Este método es equivalente a IRenderEngine:: SetRenderRange, pero toma valores de tipo Double.'
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'IRenderEngine:: SetRenderRange2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680710"
---
# <a name="irenderenginesetrenderrange2-method"></a>IRenderEngine:: SetRenderRange2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetRenderRange2` método establece el intervalo de tiempo en la escala de tiempo que se va a representar. Este método es equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), pero toma valores de tipo **Double**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de inicio, en segundos.

</dd> <dt>

*Detención* 
</dt> <dd>

Tiempo de detención, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

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

[**Interfaz IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




