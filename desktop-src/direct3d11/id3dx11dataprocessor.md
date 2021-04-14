---
title: Interfaz ID3DX11DataProcessor (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Objeto de procesamiento de datos utilizado por la interfaz ID3DX11ThreadPump para cargar datos de forma asincrónica.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interfaz ID3DX11DataProcessor Direct3D 11
- Interfaz ID3DX11DataProcessor Direct3D 11, descrita
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
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984147"
---
# <a name="id3dx11dataprocessor-interface"></a>Interfaz ID3DX11DataProcessor

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Objeto de procesamiento de datos utilizado por la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md) para cargar datos de forma asincrónica.

## <a name="members"></a>Miembros

La interfaz **ID3DX11DataProcessor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11DataProcessor** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Crea un objeto de dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataprocessor-destroy.md"><strong>Borrar</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Destruye el procesador una vez completado un elemento de trabajo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-process.md"><strong>Proceso</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Procesa los datos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Este objeto se puede heredar y sus miembros se pueden redefinir para procesar formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

