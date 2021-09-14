---
description: El método RenderOutputPins crea la parte de vista previa del gráfico de filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: Método IRenderEngine::RenderOutputPins (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886729"
---
# <a name="irenderenginerenderoutputpins-method"></a>Método IRenderEngine::RenderOutputPins

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `RenderOutputPins` método crea la parte de vista previa del gráfico de filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son los valores posibles:



| Código devuelto                                                                                                  | Descripción                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                                                        |
| <dl> <dt>**EL AUDIO DE VFW \_ S \_ NO SE \_ \_ REPRESENTA**</dt> </dl>  | No se puede reproducir la secuencia de audio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento no válido.<br/>                                               |
| <dl> <dt>**E \_ EL MOTOR DE REPRESENTACIÓN ESTÁ \_ \_ \_ ROTO**</dt> </dl> | Error en la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | error inesperado.<br/>                                               |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame [**a IRenderEngine::ConnectFrontEnd para**](irenderengine-connectfrontend.md) compilar el front-end del gráfico. Para realizar una operación que no sea la versión preliminar, no llame a este método. En su lugar, [**llame a IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para obtener punteros a los pines de salida.

Si no hay ninguna tarjeta de sonido en el equipo del usuario, este método devuelve VFW \_ S \_ AUDIO NOT \_ \_ RENDERED. En este caso, no habrá una vista previa de audio, pero la vista previa del vídeo no se verá afectada.

Si el pin es de un grupo de vídeo, este método crea una ventana de vídeo. El subproceso de llamada debe enviar mensajes, por ejemplo, para mover la ventana o responder a los clics del mouse en el área de cliente de la ventana.

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

 

 




