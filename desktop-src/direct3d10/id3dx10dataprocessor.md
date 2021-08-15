---
description: Objeto de procesamiento de datos utilizado por la interfaz ID3DX10ThreadPump para procesar los datos cargados de forma asincrónica.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaz ID3DX10DataProcessor (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128377"
---
# <a name="id3dx10dataprocessor-interface"></a>Interfaz ID3DX10DataProcessor

Objeto de procesamiento de datos utilizado [**por la interfaz ID3DX10ThreadPump para**](id3dx10threadpump.md) procesar los datos cargados de forma asincrónica.

## <a name="members"></a>Miembros

La **interfaz ID3DX10DataProcessor** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10DataProcessor** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Cree un objeto de dispositivo.<br/>                                                                                                  |
| [**Destruir**](id3dx10dataprocessor-destroy.md)                       | Lo usa una [**interfaz ID3DX10ThreadPump para**](id3dx10threadpump.md) destruir el procesador una vez completado un elemento de trabajo.<br/> |
| [**Proceso**](id3dx10dataprocessor-process.md)                       | Procesar algunos datos.<br/>                                                                                                       |



 

## <a name="remarks"></a>Comentarios

Este objeto se puede heredar y sus miembros se pueden volver a definir. Esto le permitiría personalizar la API para procesar sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
