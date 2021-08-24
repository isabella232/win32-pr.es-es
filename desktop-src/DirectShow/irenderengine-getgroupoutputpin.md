---
description: El método GetGroupOutputPin recupera el pin de salida para el grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: Método IRenderEngine::GetGroupOutputPin (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 99a1f3c60dcafdda219dc8a05f5523d7c2386249ff500bbb9abb463294ca7239
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767155"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>IRenderEngine::GetGroupOutputPin (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetGroupOutputPin` método recupera el pin de salida para el grupo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Índice de base cero que especifica el grupo.

</dd> <dt>

*ppRenderPin* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                                  | Descripción                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | El grupo no tiene un pin de salida.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento no válido.<br/>                                               |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl>       | No se pudo inicializar el motor de representación.<br/>                             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                    | Puntero no válido.<br/>                                                |
| <dl> <dt>**E \_ RENDER \_ ENGINE \_ IS \_ BROKEN**</dt> </dl> | Error en la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | error inesperado.<br/>                                               |



 

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, llame [**a IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico. Cada grupo representa un único flujo multimedia y el front-end tiene un pin de salida correspondiente.

Puede usar este método para crear la parte de representación de un gráfico de escritura de archivos. Conectar los pines de salida a filtros multiplexor y filtros de escritor de archivos. Para obtener más información, vea [Representación de un Project](rendering-a-project.md).

Para la versión preliminar, no es necesario llamar a este método. Simplemente llame **a ConnectFrontEnd** seguido de [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).

Si el método devuelve S \_ OK, la **interfaz IPin** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IRenderEngine (Interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




