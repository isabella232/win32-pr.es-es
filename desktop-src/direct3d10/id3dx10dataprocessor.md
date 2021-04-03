---
description: Objeto de procesamiento de datos utilizado por la interfaz ID3DX10ThreadPump para procesar datos cargados de forma asincrónica.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaz ID3DX10DataProcessor (D3DX10. h)
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
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914830"
---
# <a name="id3dx10dataprocessor-interface"></a>Interfaz ID3DX10DataProcessor

Objeto de procesamiento de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para procesar datos cargados de forma asincrónica.

## <a name="members"></a>Miembros

La interfaz **ID3DX10DataProcessor** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10DataProcessor** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Cree un objeto de dispositivo.<br/>                                                                                                  |
| [**Borrar**](id3dx10dataprocessor-destroy.md)                       | Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir el procesador después de que se complete un elemento de trabajo.<br/> |
| [**Proceso**](id3dx10dataprocessor-process.md)                       | Procesa algunos datos.<br/>                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Este objeto se puede heredar y sus miembros se pueden redefinir. Esto le permitirá personalizar la API para procesar sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
