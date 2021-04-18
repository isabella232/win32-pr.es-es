---
description: El método ConnectFrontEnd crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine:: ConnectFrontEnd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680616"
---
# <a name="irenderengineconnectfrontend-method"></a>IRenderEngine:: ConnectFrontEnd (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ConnectFrontEnd` método crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los posibles valores devueltos se incluyen los siguientes:



| Código devuelto                                                                                                  | Descripción                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                                                            |
| <dl> <dt>**S \_ WARN \_ OUTPUTRESET**</dt> </dl>          | Se eliminó la parte de representación del gráfico.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | No se ha establecido una escala de tiempo para este motor de representación.<br/>                             |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl>       | No se pudo inicializar el motor de representación.<br/>                                 |
| <dl> <dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt> </dl> | No se pudo realizar la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>                 | error inesperado.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo de medio no válido.<br/>                                                 |



 

## <a name="remarks"></a>Observaciones

Este método no genera la parte de representación del gráfico de filtro. La aplicación debe conectar los pin de salida en el front-end a los filtros de representación deseados:

-   Para obtener una vista previa, llame al método [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .
-   Para generar un archivo, llame a [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar el PIN de salida de cada grupo y, a continuación, conecte los pin a un filtro de multiplexor.

Si usa el motor de representación básico, los terminales de salida del front-end generan datos sin comprimir. Si usa el motor de representación inteligente, los pin de salida generan datos comprimidos.

Si cambia la escala de tiempo después de compilar el gráfico de filtros, debe volver a llamar `ConnectFrontEnd` a para volver a generar el front-end. El método conserva la parte de representación del gráfico siempre que sea posible. Sin embargo, si agrega o elimina un grupo, o cambia el orden de los grupos, `ConnectFrontEnd` elimina la parte de representación y la aplicación debe recompilarla. Si el método elimina la parte de representación, devuelve S \_ WARN \_ OUTPUTRESET.

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

 

 




