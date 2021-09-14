---
description: El método SetRenderRange2 establece el intervalo de tiempo en la escala de tiempo que se va a representar. Este método es equivalente a IRenderEngine::SetRenderRange, pero toma valores de tipo double.
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: Método IRenderEngine::SetRenderRange2 (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886673"
---
# <a name="irenderenginesetrenderrange2-method"></a>IRenderEngine::SetRenderRange2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetRenderRange2` método establece el intervalo de tiempo en la escala de tiempo que se va a representar. Este método es equivalente a [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), pero toma valores de tipo **double**.

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

Tiempo de detenerse, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




