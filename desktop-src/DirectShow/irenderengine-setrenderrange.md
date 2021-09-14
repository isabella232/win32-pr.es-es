---
description: El método SetRenderRange establece el intervalo de tiempo en la escala de tiempo que se va a representar. Los objetos que se encuentran fuera del intervalo especificado no se representan y no se les asignan recursos.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: Método IRenderEngine::SetRenderRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886676"
---
# <a name="irenderenginesetrenderrange-method"></a>IRenderEngine::SetRenderRange (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetRenderRange` método establece el intervalo de tiempo de la escala de tiempo que se va a representar. Los objetos que se encuentran fuera del intervalo especificado no se representan y no se les asignan recursos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de inicio, en unidades de 100 nanosegundos.

</dd> <dt>

*Detención* 
</dt> <dd>

Tiempo de detenerse, en unidades de 100 nanosegundos.

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

[**IRenderEngine (Interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




