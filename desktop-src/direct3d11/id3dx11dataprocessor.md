---
title: Interfaz ID3DX11DataProcessor (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Objeto de procesamiento de datos utilizado por la interfaz ID3DX11ThreadPump para cargar datos de forma asincrónica.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interfaz ID3DX11DataProcessor Direct3D 11
- Interfaz ID3DX11DataProcessor direct3D 11 , descrito
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 808c7d1bf1bdef1223e5b57e40ea5e6a90878101
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966912"
---
# <a name="id3dx11dataprocessor-interface"></a>Interfaz ID3DX11DataProcessor

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Objeto de procesamiento de datos utilizado [**por la interfaz ID3DX11ThreadPump para**](id3dx11threadpump.md) cargar datos de forma asincrónica.

## <a name="members"></a>Members

La **interfaz ID3DX11DataProcessor** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11DataProcessor** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Crea un objeto de dispositivo.<br /> | 
| <a href="id3dx11dataprocessor-destroy.md"><strong>Destruir</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Destruye el procesador una vez completado un elemento de trabajo.<br /> | 
| <a href="id3dx11dataprocessor-process.md"><strong>Proceso</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Procesa los datos.<br /> | 




 

## <a name="remarks"></a>Observaciones

Este objeto se puede heredar y sus miembros se pueden volver a definir para procesar formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

