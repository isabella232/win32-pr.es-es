---
description: El método RenderOutputPins crea la parte de vista previa del gráfico de filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine:: RenderOutputPins (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680714"
---
# <a name="irenderenginerenderoutputpins-method"></a>IRenderEngine:: RenderOutputPins (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `RenderOutputPins` método crea la parte de vista previa del gráfico de filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son los valores posibles:



| Código devuelto                                                                                                  | Descripción                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                                                        |
| <dl> <dt>**\_no se \_ representa el audio VFW S \_ \_**</dt> </dl>  | No se puede reproducir la secuencia de audio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento no válido.<br/>                                               |
| <dl> <dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt> </dl> | No se pudo realizar la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>                 | error inesperado.<br/>                                               |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico. Para realizar una operación distinta de la vista previa, no llame a este método. En su lugar, llame a [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para obtener punteros a los pin de salida.

Si no hay ninguna tarjeta de sonido en el equipo del usuario, este método devuelve VFW \_ s \_ audio \_ no \_ representado. En este caso, no habrá vista previa de audio, pero la vista previa de vídeo no se ve afectada.

Si el PIN es de un grupo de vídeos, este método crea una ventana de vídeo. El subproceso que realiza la llamada debe enviar los mensajes (por ejemplo, para desplace la ventana o responder a los clics del mouse en el área cliente de la ventana).

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

 

 




