---
description: El método ConnectFrontEnd compila el front-end del gráfico de filtros a partir de la escala de tiempo actual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: Método IRenderEngine::ConnectFrontEnd (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160147"
---
# <a name="irenderengineconnectfrontend-method"></a>IRenderEngine::ConnectFrontEnd (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `ConnectFrontEnd` método compila el front-end del gráfico de filtros a partir de la escala de tiempo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores devueltos posibles se incluyen los siguientes:



| Código devuelto                                                                                                  | Descripción                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                                                            |
| <dl> <dt>**S \_ WARN \_ OUTPUTRESET**</dt> </dl>          | Se eliminó la parte de representación del gráfico.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | No se ha establecido ninguna escala de tiempo para este motor de representación.<br/>                             |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl>       | No se pudo inicializar el motor de representación.<br/>                                 |
| <dl> <dt>**E \_ EL MOTOR DE REPRESENTACIÓN ESTÁ \_ \_ \_ ROTO**</dt> </dl> | Error en la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | error inesperado.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo de medio no válido.<br/>                                                 |



 

## <a name="remarks"></a>Observaciones

Este método no compila la parte de representación del gráfico de filtro. La aplicación debe conectar los pines de salida del front-end a los filtros de representación deseados:

-   Para obtener una vista previa, llame [**al método IRenderEngine::RenderOutputPins.**](irenderengine-renderoutputpins.md)
-   Para generar un archivo, llame a [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar el pin de salida de cada grupo y, a continuación, conecte los pines a un filtro de multiplexor.

Si usa el motor de representación básico, los pines de salida del front-end generan datos sin comprimir. Si usa el motor de representación inteligente, las patillas de salida generan datos comprimidos.

Si cambia la escala de tiempo después de compilar el gráfico de filtros, debe llamar de nuevo a para volver a `ConnectFrontEnd` generar el front-end. El método conserva la parte de representación del gráfico siempre que sea posible. Sin embargo, si agrega o elimina un grupo, o cambia el orden de los grupos, elimina la parte de representación y la aplicación debe volver a `ConnectFrontEnd` generarlo. Si el método elimina la parte de representación, devuelve S \_ WARN \_ OUTPUTRESET.

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

 

 




